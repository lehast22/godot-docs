.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the FileDialog.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_FileDialog:

FileDialog
==========

**Inherits:** :ref:`ConfirmationDialog<class_confirmationdialog>` **<** :ref:`AcceptDialog<class_acceptdialog>` **<** :ref:`WindowDialog<class_windowdialog>` **<** :ref:`Popup<class_popup>` **<** :ref:`Control<class_control>` **<** :ref:`CanvasItem<class_canvasitem>` **<** :ref:`Node<class_node>` **<** :ref:`Object<class_object>`

**Category:** Core

Brief Description
-----------------

Dialog for selecting files or directories in the filesystem.

Member Functions
----------------

+--------------------------------------------+-----------------------------------------------------------------------------------------------+
| void                                       | :ref:`add_filter<class_FileDialog_add_filter>` **(** :ref:`String<class_string>` filter **)** |
+--------------------------------------------+-----------------------------------------------------------------------------------------------+
| void                                       | :ref:`clear_filters<class_FileDialog_clear_filters>` **(** **)**                              |
+--------------------------------------------+-----------------------------------------------------------------------------------------------+
| void                                       | :ref:`deselect_items<class_FileDialog_deselect_items>` **(** **)**                            |
+--------------------------------------------+-----------------------------------------------------------------------------------------------+
| :ref:`VBoxContainer<class_vboxcontainer>`  | :ref:`get_vbox<class_FileDialog_get_vbox>` **(** **)**                                        |
+--------------------------------------------+-----------------------------------------------------------------------------------------------+
| void                                       | :ref:`invalidate<class_FileDialog_invalidate>` **(** **)**                                    |
+--------------------------------------------+-----------------------------------------------------------------------------------------------+

Signals
-------

.. _class_FileDialog_dir_selected:

- **dir_selected** **(** :ref:`String<class_string>` dir **)**

Event emitted when the user selects a directory.

.. _class_FileDialog_file_selected:

- **file_selected** **(** :ref:`String<class_string>` path **)**

Event emitted when the user selects a file (double clicks it or presses the OK button).

.. _class_FileDialog_files_selected:

- **files_selected** **(** :ref:`PoolStringArray<class_poolstringarray>` paths **)**

Event emitted when the user selects multiple files.


Member Variables
----------------

  .. _class_FileDialog_access:

- :ref:`Access<enum_filedialog_access>` **access**

  .. _class_FileDialog_current_dir:

- :ref:`String<class_string>` **current_dir** - The current working directory of the file dialog.

  .. _class_FileDialog_current_file:

- :ref:`String<class_string>` **current_file** - The currently selected file of the file dialog.

  .. _class_FileDialog_current_path:

- :ref:`String<class_string>` **current_path** - The currently selected file path of the file dialog.

  .. _class_FileDialog_filters:

- :ref:`PoolStringArray<class_poolstringarray>` **filters**

  .. _class_FileDialog_mode:

- :ref:`Mode<enum_filedialog_mode>` **mode**

  .. _class_FileDialog_mode_overrides_title:

- :ref:`bool<class_bool>` **mode_overrides_title** - If ``true``, changing the ``mode`` property will set the window title accordingly (e. g. setting mode to ``MODE_OPEN_FILE`` will change the window title to "Open a File").

  .. _class_FileDialog_show_hidden_files:

- :ref:`bool<class_bool>` **show_hidden_files**


Enums
-----

  .. _enum_FileDialog_Access:

enum **Access**

- **ACCESS_RESOURCES** = **0** --- The dialog allows the selection of file and directory.
- **ACCESS_USERDATA** = **1** --- The dialog allows access files under :ref:`Resource<class_resource>` path(res://) .
- **ACCESS_FILESYSTEM** = **2** --- The dialog allows access files in whole file system.

  .. _enum_FileDialog_Mode:

enum **Mode**

- **MODE_OPEN_FILE** = **0** --- The dialog allows the selection of one, and only one file.
- **MODE_OPEN_FILES** = **1** --- The dialog allows the selection of multiple files.
- **MODE_OPEN_DIR** = **2** --- The dialog functions as a folder selector, disallowing the selection of any file.
- **MODE_OPEN_ANY** = **3** --- The dialog allows the selection of a file or a directory.
- **MODE_SAVE_FILE** = **4** --- The dialog will warn when a file exists.


Description
-----------

FileDialog is a preset dialog used to choose files and directories in the filesystem. It supports filter masks.

Member Function Description
---------------------------

.. _class_FileDialog_add_filter:

- void **add_filter** **(** :ref:`String<class_string>` filter **)**

Add a custom filter. Filter format is: "mask ; description", example (C++): dialog->add_filter("\*.png ; PNG Images");

.. _class_FileDialog_clear_filters:

- void **clear_filters** **(** **)**

Clear all the added filters in the dialog.

.. _class_FileDialog_deselect_items:

- void **deselect_items** **(** **)**

.. _class_FileDialog_get_vbox:

- :ref:`VBoxContainer<class_vboxcontainer>` **get_vbox** **(** **)**

Return the vertical box container of the dialog, custom controls can be added to it.

.. _class_FileDialog_invalidate:

- void **invalidate** **(** **)**

Invalidate and update the current dialog content list.


