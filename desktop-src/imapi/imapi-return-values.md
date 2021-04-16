---
title: IMAPI-Rückgabewerte (Imapi2error. h)
description: Die IMAPI-Methoden geben nicht negative Werte zurück (in der Regel ist dies \_ OK), wenn die Methode erfolgreich war. Die IMAPI-Methoden geben Erfolgs-oder Fehlercodes von Winerror. h, Imapi2error. h oder Imapi2fserror. h bei einem Fehler zurück.
ms.assetid: 0e62ed6c-4810-4d36-a759-9b02b68face6
topic_type:
- apiref
api_name:
- E_IMAPI_BURN_VERIFICATION_FAILED
- E_IMAPI_REQUEST_CANCELLED
- E_IMAPI_RECORDER_REQUIRED
- S_IMAPI_WRITE_NOT_IN_PROGRESS
- S_IMAPI_SPEEDADJUSTED
- S_IMAPI_ROTATIONADJUSTED
- S_IMAPI_BOTHADJUSTED
- S_IMAPI_COMMAND_HAS_SENSE_DATA
- E_IMAPI_RAW_IMAGE_IS_READ_ONLY
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS
- E_IMAPI_RAW_IMAGE_NO_TRACKS
- E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED
- E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED
- E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE
- E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND
- S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED
- E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX
- E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE
- E_IMAPI_RECORDER_MEDIA_NO_MEDIA
- E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE
- E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN
- E_IMAPI_RECORDER_MEDIA_BECOMING_READY
- E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS
- E_IMAPI_RECORDER_MEDIA_BUSY
- E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS
- E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED
- E_IMAPI_RECORDER_NO_SUCH_FEATURE
- E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT
- E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED
- E_IMAPI_RECORDER_COMMAND_TIMEOUT
- E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT
- E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH
- E_IMAPI_RECORDER_LOCKED
- E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE
- E_IMAPI_LOSS_OF_STREAMING
- E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE
- E_IMAPI_DF2DATA_WRITE_IN_PROGRESS
- E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2DATA_INVALID_MEDIA_STATE
- E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA
- E_IMAPI_DF2DATA_MEDIA_NOT_BLANK
- E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2TAO_WRITE_IN_PROGRESS
- E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2TAO_MEDIA_IS_PREPARED
- E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY
- E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED
- E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE
- E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2TAO_INVALID_ISRC
- E_IMAPI_DF2TAO_INVALID_MCN
- E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED
- E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_WRITE_IN_PROGRESS
- E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED
- E_IMAPI_DF2RAW_MEDIA_IS_PREPARED
- E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK
- E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE
- E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED
- E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED
- E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED
- E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT
- E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_IN_USE
- E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED
- E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL
- E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL
- E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE
- E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND
- E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR
- E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE
- E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND
- E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED
- E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED
- E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID
- IMAPI_E_FSI_INTERNAL_ERROR
- IMAPI_E_INVALID_PARAM
- IMAPI_E_READONLY
- IMAPI_E_NO_OUTPUT
- IMAPI_E_INVALID_VOLUME_NAME
- IMAPI_E_INVALID_DATE
- IMAPI_E_FILE_SYSTEM_NOT_EMPTY
- IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED
- IMAPI_E_NOT_FILE
- IMAPI_E_NOT_DIR
- IMAPI_E_DIR_NOT_EMPTY
- IMAPI_E_NOT_IN_FILE_SYSTEM
- IMAPI_E_INVALID_PATH
- IMAPI_E_RESTRICTED_NAME_VIOLATION
- IMAPI_E_DUP_NAME
- IMAPI_E_NO_UNIQUE_NAME
- IMAPI_E_ITEM_NOT_FOUND
- IMAPI_E_FILE_NOT_FOUND
- IMAPI_E_DIR_NOT_FOUND
- IMAPI_E_IMAGE_SIZE_LIMIT
- IMAPI_E_IMAGE_TOO_BIG
- IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED
- IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND
- IMAPI_E_IMAGEMANAGER_NO_IMAGE
- IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG
- IMAPI_E_DATA_STREAM_INCONSISTENCY
- IMAPI_E_DATA_STREAM_READ_FAILURE
- IMAPI_E_DATA_STREAM_CREATE_FAILURE
- IMAPI_E_DIRECTORY_READ_FAILURE
- IMAPI_E_TOO_MANY_DIRS
- IMAPI_E_ISO9660_LEVELS
- IMAPI_E_DATA_TOO_BIG
- IMAPI_E_STASHFILE_OPEN_FAILURE
- IMAPI_E_STASHFILE_SEEK_FAILURE
- IMAPI_E_STASHFILE_WRITE_FAILURE
- IMAPI_E_STASHFILE_READ_FAILURE
- IMAPI_E_INVALID_WORKING_DIRECTORY
- IMAPI_E_WORKING_DIRECTORY_SPACE
- IMAPI_E_STASHFILE_MOVE
- IMAPI_E_BOOT_IMAGE_DATA
- IMAPI_E_BOOT_OBJECT_CONFLICT
- IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH
- IMAPI_E_EMPTY_DISC
- IMAPI_E_NO_SUPPORTED_FILE_SYSTEM
- IMAPI_E_FILE_SYSTEM_NOT_FOUND
- IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR
- IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED
- IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY
- IMAPI_E_IMPORT_SEEK_FAILURE
- IMAPI_E_IMPORT_READ_FAILURE
- IMAPI_E_DISC_MISMATCH
- IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED
- IMAPI_E_UDF_NOT_WRITE_COMPATIBLE
- IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION
- IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE
- IMAPI_E_MULTISESSION_NOT_SET
- IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE
- IMAPI_E_BAD_MULTISESSION_PARAMETER
- IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED
api_location:
- Imapi2error.h
- Imapi2fserror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6bc4b99bb5ac123ea26ca1deb755fa29598811b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477160"
---
# <a name="imapi-return-values"></a>IMAPI-Rückgabewerte

Die IMAPI-Methoden geben nicht negative Werte zurück (in der Regel ist dies \_ OK), wenn die Methode erfolgreich war. Die IMAPI-Methoden geben Erfolgs-oder Fehlercodes von Winerror. h, Imapi2error. h oder Imapi2fserror. h bei einem Fehler zurück.

Die folgenden Erfolgs-und Fehlercodes sind definiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl> <dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT) 0xc0aa0007l</dt> </dl></td>
<td style="text-align: left;">Der Datenträger hat die Überprüfung der Überprüfung nicht bestanden und kann beschädigte Daten enthalten oder nicht verwendbar sein.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl> <dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT) 0xc0aa0002</dt> </dl></td>
<td style="text-align: left;">Die Anforderung wurde abgebrochen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl> <dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT) 0xc0aa0003</dt> </dl></td>
<td style="text-align: left;">Für die Anforderung muss eine aktuelle Disc Recorder ausgewählt werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl> <dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0x00aa0302l</dt> </dl></td>
<td style="text-align: left;">Zurzeit wird kein Schreibvorgang ausgeführt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl> <dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT) 0x00aa0004</dt> </dl></td>
<td style="text-align: left;">Die angeforderte Schreibgeschwindigkeit wurde vom Laufwerk nicht unterstützt, und die Geschwindigkeit wurde angepasst.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl> <dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT) 0x00aa0005</dt> </dl></td>
<td style="text-align: left;">Der angeforderte drehungstyp wurde vom Laufwerk nicht unterstützt, und der drehtyp wurde angepasst.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl> <dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT) 0x00aa0006</dt> </dl></td>
<td style="text-align: left;">Die angeforderte Schreibgeschwindigkeit und der drehtyp wurden vom Laufwerk nicht unterstützt, und beide wurden angepasst.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl> <dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT) 0x00aa0200</dt> </dl></td>
<td style="text-align: left;">Das Gerät hat den Befehl akzeptiert, hat jedoch die Sense-Daten zurückgegeben, die auf einen Fehler hinweisen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT) 0x80aa0a00l</dt> </dl></td>
<td style="text-align: left;">Das Image ist aufgrund eines Aufrufes durch einen Aufrufen von <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>irawcdimagecreator:: kreateresultimage</strong></a>schreibgeschützt. Daher kann das Objekt nicht mehr geändert werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT) 0x80aa0a01l</dt> </dl></td>
<td style="text-align: left;">Es können keine weiteren Spuren hinzugefügt werden. CD-Medien sind auf einen Bereich von 1-99-Spuren beschränkt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT) 0x80aa0a03l</dt> </dl></td>
<td style="text-align: left;">Vor der Verwendung dieser Funktion müssen dem bildspuren hinzugefügt werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80aa0a02l</dt> </dl></td>
<td style="text-align: left;">Der angeforderte sektortyp wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT) 0x80aa0a04l</dt> </dl></td>
<td style="text-align: left;">Vor der Verwendung dieser Funktion können dem Bild keine Spuren hinzugefügt werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT) 0x80aa0a05l</dt> </dl></td>
<td style="text-align: left;">Durch das Hinzufügen dieses Titels würden die Einschränkungen des Starts der Leadout-Eigenschaft überschritten.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT) 0x80aa0a06l</dt> </dl></td>
<td style="text-align: left;">Durch das Hinzufügen dieses Titels würde die Index Grenze von 99 überschritten.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT) 0x80aa0a07l</dt> </dl></td>
<td style="text-align: left;">Der angegebene LBA-Offset ist nicht in der Liste der Nachverfolgung-Indizes enthalten.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl> <dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT) 0x00aa0a08l</dt> </dl></td>
<td style="text-align: left;">Der angegebene LBA-Offset befindet sich bereits in der Liste der Nachverfolgung-Indizes.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT) 0x80aa0a09l</dt> </dl></td>
<td style="text-align: left;">Der Index 1 (LBA-Offset NULL) kann nicht gelöscht werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl> <dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT) 0x80aa0a0al</dt> </dl></td>
<td style="text-align: left;">Jeder Index muss über eine minimale Größe von zehn Sektoren verfügen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl> <dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT) 0xc0aa0201</dt> </dl></td>
<td style="text-align: left;">Das Gerät hat gemeldet, dass die Seite angeforderter Modus (und Typ) nicht vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl> <dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT) 0xc0aa0202</dt> </dl></td>
<td style="text-align: left;">Es ist kein Medium auf dem Gerät vorhanden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl> <dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT) 0xc0aa0203</dt> </dl></td>
<td style="text-align: left;">Das Medium ist nicht kompatibel oder weist ein unbekanntes physisches Format auf.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl> <dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT) 0xc0aa0204</dt> </dl></td>
<td style="text-align: left;">Das Medium wird nach oben eingefügt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl> <dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT) 0xc0aa0205</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat gemeldet, dass es gerade bereit ist. Wiederholen Sie die Anforderung später.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl> <dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0206</dt> </dl></td>
<td style="text-align: left;">Das Medium wird zurzeit formatiert. Warten Sie, bis das Format fertiggestellt wurde, bevor Sie versuchen, die Medien zu verwenden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl> <dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT) 0xc0aa0207</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat gemeldet, dass es einen Vorgang mit langer Laufzeit ausführt, z. b. das Abschließen eines Schreibvorgangs. Das Laufwerk ist möglicherweise für längere Zeit unbrauchbar.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl> <dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT) 0xc0aa0208</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat gemeldet, dass die Kombination der Parameter, die auf der Seite Modus für einen Modus SELECT-Befehl angegeben wurde, nicht unterstützt wird<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl> <dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT) 0xc0aa0209</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat gemeldet, dass das Medium schreibgeschützt ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl> <dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT) 0xc0aa020a</dt> </dl></td>
<td style="text-align: left;">Die angeforderte funktionsseite wird vom Gerät nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl> <dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT) 0xc0aa020b</dt> </dl></td>
<td style="text-align: left;">Die angeforderte funktionsseite wird unterstützt, aber nicht als aktuell gekennzeichnet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl> <dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa020c</dt> </dl></td>
<td style="text-align: left;">Der Befehl "Get Configuration" wird vom Laufwerk nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl> <dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT) 0xc0aa020d</dt> </dl></td>
<td style="text-align: left;">Das Gerät konnte den Befehl innerhalb des Timeout Zeitraums nicht akzeptieren. Dies kann darauf zurückzuführen sein, dass das Gerät in einen inkonsistenten Status eingetreten ist, oder dass der Timeout Wert für den Befehl möglicherweise gesteigert werden muss.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl> <dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT) 0xc0aa020E</dt> </dl></td>
<td style="text-align: left;">Die DVD-Struktur ist nicht vorhanden. Dies kann durch nicht verwendetes nicht verwendetes Laufwerk/Medium verursacht werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl> <dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT) 0xc0aa020f</dt> </dl></td>
<td style="text-align: left;">Die Geschwindigkeit des Mediums ist mit dem Gerät nicht kompatibel. Dies kann durch die Verwendung eines höheren oder niedrigeren Geschwindigkeits Mediums verursacht werden, als der vom Gerät unterstützte Bereich von Geschwindigkeiten.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl> <dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT) 0xc0aa0210</dt> </dl></td>
<td style="text-align: left;">Das Gerät, das dieser Aufzeichnung während des letzten Vorgangs zugeordnet ist, wurde exklusiv gesperrt und führt zu einem Fehler bei diesem Vorgang.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl> <dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa0211</dt> </dl></td>
<td style="text-align: left;">Der Client Name ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl> <dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xc0aa02ff</dt> </dl></td>
<td style="text-align: left;">Das Gerät meldete unerwartete oder ungültige Daten für einen Befehl.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl> <dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT) 0xc0aa0300</dt> </dl></td>
<td style="text-align: left;">Der Schreibvorgang ist fehlgeschlagen, da das Laufwerk keine Daten schnell genug empfangen hat, um das Schreiben fortzusetzen. Wenn Sie die Quelldaten auf den lokalen Computer verschieben, die Schreibgeschwindigkeit reduzieren oder eine &quot; Einstellung für einen Pufferunterlauf freigeben, &quot; kann dieses Problem möglicherweise behoben werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl> <dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xc0aa0301</dt> </dl></td>
<td style="text-align: left;">Das Schreiben ist fehlgeschlagen, weil das Laufwerk Fehlerinformationen zurückgegeben hat, die nicht von wieder hergestellt werden konnten.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl> <dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0400</dt> </dl></td>
<td style="text-align: left;">Zurzeit wird ein Schreibvorgang ausgeführt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl> <dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0401</dt> </dl></td>
<td style="text-align: left;">Zurzeit wird kein Schreibvorgang ausgeführt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl> <dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT) 0xc0aa0402</dt> </dl></td>
<td style="text-align: left;">Der angeforderte Vorgang ist nur mit unterstützten Medien gültig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0403</dt> </dl></td>
<td style="text-align: left;">Der bereitgestellte zu schreibende Datenstrom wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl> <dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT) 0xc0aa0404</dt> </dl></td>
<td style="text-align: left;">Der bereitgestellte zu schreibende Stream ist zu groß für die aktuell eingefügten Medien.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl> <dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xc0aa0405</dt> </dl></td>
<td style="text-align: left;">Das Überschreiben von nicht leeren Medien ist nicht zulässig, ohne dass die Eigenschaft forceüberschreibung auf VARIANT_TRUE festgelegt ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0406</dt> </dl></td>
<td style="text-align: left;">Der aktuelle Medientyp wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0407</dt> </dl></td>
<td style="text-align: left;">Dieses Gerät unterstützt nicht die Vorgänge, die für dieses Festplatten Format erforderlich sind.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl> <dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa0408</dt> </dl></td>
<td style="text-align: left;">Der Client Name ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl> <dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0500</dt> </dl></td>
<td style="text-align: left;">Zurzeit wird ein Schreibvorgang ausgeführt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl> <dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0501</dt> </dl></td>
<td style="text-align: left;">Zurzeit wird kein Schreibvorgang ausgeführt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl> <dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xc0aa0502</dt> </dl></td>
<td style="text-align: left;">Der angeforderte Vorgang ist nur gültig, wenn Medien &quot; vorbereitet wurden &quot; .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl> <dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xc0aa0503</dt> </dl></td>
<td style="text-align: left;">Der angeforderte Vorgang ist ungültig, wenn Medien &quot; vorbereitet, &quot; aber nicht freigegeben wurden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl> <dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT) 0xc0aa0504</dt> </dl></td>
<td style="text-align: left;">Die-Eigenschaft kann nicht geändert werden, nachdem auf das Medium geschrieben wurde.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl> <dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xc0aa0505</dt> </dl></td>
<td style="text-align: left;">Das Inhaltsverzeichnis kann nicht von einem leeren Laufwerk abgerufen werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl> <dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xc0aa0506</dt> </dl></td>
<td style="text-align: left;">Es werden nur leere CD-R/RW-Medien unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0507</dt> </dl></td>
<td style="text-align: left;">Es werden nur leere CD-R/RW-Medien unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl> <dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT) 0xc0aa0508</dt> </dl></td>
<td style="text-align: left;">CD-R-und CD-RW-Medien unterstützen maximal 99 Audiospuren.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl> <dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xc0aa0509</dt> </dl></td>
<td style="text-align: left;">Auf dem Medium ist nicht genügend Speicherplatz vorhanden, um die bereitgestellte Audiospur hinzuzufügen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl> <dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xc0aa050a</dt> </dl></td>
<td style="text-align: left;">Sie können das Medium erst vorbereiten, nachdem Sie eine Aufzeichnung ausgewählt haben.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl> <dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT) 0xc0aa050b</dt> </dl></td>
<td style="text-align: left;">Der angegebene ISRC-Wert ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl> <dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT) 0xc0aa050c</dt> </dl></td>
<td style="text-align: left;">Die angegebene Medienkatalog Nummer ist ungültig.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa050d</dt> </dl></td>
<td style="text-align: left;">Der bereitgestellte Audiodatenstrom ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa050E</dt> </dl></td>
<td style="text-align: left;">Dieses Gerät unterstützt nicht die Vorgänge, die für dieses Festplatten Format erforderlich sind.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl> <dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa050f</dt> </dl></td>
<td style="text-align: left;">Der Client Name ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl> <dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0600</dt> </dl></td>
<td style="text-align: left;">Zurzeit wird ein Schreibvorgang ausgeführt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl> <dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0601</dt> </dl></td>
<td style="text-align: left;">Zurzeit wird kein Schreibvorgang ausgeführt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl> <dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xc0aa0602</dt> </dl></td>
<td style="text-align: left;">Der angeforderte Vorgang ist nur gültig, wenn Medien &quot; vorbereitet wurden &quot; .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl> <dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xc0aa0603</dt> </dl></td>
<td style="text-align: left;">Der angeforderte Vorgang ist ungültig, wenn Medien &quot; vorbereitet, &quot; aber nicht freigegeben wurden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl> <dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa0604</dt> </dl></td>
<td style="text-align: left;">Der Client Name ist ungültig.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl> <dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xc0aa0606</dt> </dl></td>
<td style="text-align: left;">Es werden nur leere CD-R/RW-Medien unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0607</dt> </dl></td>
<td style="text-align: left;">Es werden nur leere CD-R/RW-Medien unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl> <dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xc0aa0609</dt> </dl></td>
<td style="text-align: left;">Es ist nicht genügend Speicherplatz auf dem Medium vorhanden, um die angegebene Sitzung hinzuzufügen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl> <dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xc0aa060a</dt> </dl></td>
<td style="text-align: left;">Sie können das Medium erst vorbereiten, nachdem Sie eine Aufzeichnung ausgewählt haben.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa060d</dt> </dl></td>
<td style="text-align: left;">Der bereitgestellte Audiodatenstrom ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa060E</dt> </dl></td>
<td style="text-align: left;">Der angeforderte Daten Blocktyp wird vom aktuellen Gerät nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl> <dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT) 0xc0aa060f</dt> </dl></td>
<td style="text-align: left;">Der Stream enthält keine ausreichende Anzahl von Sektoren im Leadin für das aktuelle Medium.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl> <dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0610</dt> </dl></td>
<td style="text-align: left;">Dieses Gerät unterstützt nicht die Vorgänge, die für dieses Festplatten Format erforderlich sind.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl> <dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT) 0x80aa0900</dt> </dl></td>
<td style="text-align: left;">Das Format verwendet derzeit den Disk Recorder für einen Löschvorgang. Warten Sie, bis der Löschvorgang beendet ist, bevor Sie versuchen, den aktuellen Disk Recorder festzulegen oder zu löschen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl> <dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80aa0901</dt> </dl></td>
<td style="text-align: left;">Das Lösch Format unterstützt nur eine Aufzeichnung. Sie müssen den aktuellen Recorder löschen, bevor Sie einen neuen festgelegt haben.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl> <dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80aa0902</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat nicht genügend Daten für einen Befehl zum Lesen von Festplatten Informationen gemeldet. Das Laufwerk wird möglicherweise nicht unterstützt, oder die Medien sind möglicherweise nicht korrekt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl> <dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80aa0903</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat nicht genügend Daten für einen modussense-Befehl (Page 0x2A) gemeldet. Das Laufwerk wird möglicherweise nicht unterstützt, oder die Medien sind möglicherweise nicht korrekt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl> <dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT) 0x80aa0904</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat gemeldet, dass das Medium nicht Lösch fähig ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl> <dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT) 0x80aa0905</dt> </dl></td>
<td style="text-align: left;">Der Löschbefehl des Laufwerks ist fehlgeschlagen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl> <dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT) 0x80aa0906</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat das Löschen innerhalb einer Stunde nicht vervollständigt. Für das Laufwerk ist möglicherweise ein Energie-und Entfernungs Vorgang oder ein anderer manueller Eingriff erforderlich, um den ordnungsgemäßen Betrieb fortzusetzen<br/>
<blockquote>
[!Note]<br />
Dieser Wert wird derzeit auch zurückgegeben, wenn der Versuch, ein Löschvorgang auf CD-RW-oder DVD-RW-Medien über die <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> -Schnittstelle durchzuführen, aufgrund eines ungültigen Mediums fehlschlägt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl> <dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT) 0x80aa0907</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat während des Löschvorgangs einen unerwarteten Fehler zurückgegeben. Möglicherweise sind die Medien nicht verwendbar, der Löschvorgang ist möglicherweise noch nicht möglich, oder das Laufwerk ist dabei, die Festplatte zu löschen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl> <dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT) 0x80aa0908</dt> </dl></td>
<td style="text-align: left;">Das Laufwerk hat einen Fehler für einen Start Unit (SpinUp)-Befehl zurückgegeben. Möglicherweise ist ein manueller Eingriff erforderlich.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl> <dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0909</dt> </dl></td>
<td style="text-align: left;">Der aktuelle Medientyp wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl> <dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa090a</dt> </dl></td>
<td style="text-align: left;">Dieses Gerät unterstützt nicht die Vorgänge, die für dieses Festplatten Format erforderlich sind.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl> <dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa090b</dt> </dl></td>
<td style="text-align: left;">Der Client Name ist ungültig.<br/></td>
</tr>
</tbody>
</table>



Die folgenden Erfolgs-und Fehlercodes sind in Imapi2fserror. h definiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl> <dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT) 0xc0aab100</dt> </dl></td>
<td style="text-align: left;">Interner Fehler: %1! ls!.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl> <dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT) 0xc0aab101</dt> </dl></td>
<td style="text-align: left;">Der für den Parameter "%1! ls!" angegebene Wert. ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl> <dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT) 0xc0aab102</dt> </dl></td>
<td style="text-align: left;">Das filesystemimage-Objekt befindet sich im schreibgeschützten Modus.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl> <dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT) 0xc0aab103</dt> </dl></td>
<td style="text-align: left;">Es wurde kein Ausgabedatei System angegeben.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl> <dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT) 0xc0aab104</dt> </dl></td>
<td style="text-align: left;">Die angegebene Volumekennung ist entweder zu lang oder enthält mindestens ein ungültiges Zeichen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl> <dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT) 0xc0aab105</dt> </dl></td>
<td style="text-align: left;">Ungültige Datumsangaben. %1! ls! die Uhrzeit liegt vor %2! ls! kann.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl> <dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xc0aab106</dt> </dl></td>
<td style="text-align: left;">Das Dateisystem muss für diese Funktion leer sein.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl> <dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xc0aab163l</dt> </dl></td>
<td style="text-align: left;">Sie können das für die Erstellung angegebene Dateisystem nicht ändern, da das Dateisystem aus der importierten Sitzung und das Dateisystem in der aktuellen Sitzung nicht mit identisch sind.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl> <dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT) 0xc0aab108</dt> </dl></td>
<td style="text-align: left;">Der angegebene Pfad "%1! ls!". identifiziert keine Datei.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl> <dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT) 0xc0aab109</dt> </dl></td>
<td style="text-align: left;">Der angegebene Pfad "%1! ls!". identifiziert kein Verzeichnis.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl> <dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xc0aab10a</dt> </dl></td>
<td style="text-align: left;">Das Verzeichnis "%1! s!". ist nicht leer.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl> <dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xc0aab10b</dt> </dl></td>
<td style="text-align: left;">ls! " ist nicht Teil des Dateisystems. Sie muss hinzugefügt werden, um diesen Vorgang abzuschließen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl> <dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT) 0xc0aab110</dt> </dl></td>
<td style="text-align: left;">Pfad "%1! s!" ist falsch formatiert oder enthält ungültige Zeichen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl> <dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT) 0xc0aab111</dt> </dl></td>
<td style="text-align: left;">Der Name "%1! ls!" angegeben ist nicht zulässig: der Name der Datei oder des Verzeichnis Objekts, das erstellt wird, während die userestrictedcharakteriset-Eigenschaft festgelegt ist, darf nur ANSI-Zeichen enthalten.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl> <dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT) 0xc0aab112</dt> </dl></td>
<td style="text-align: left;">ls! " der Name ist bereits vorhanden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl> <dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT) 0xc0aab113</dt> </dl></td>
<td style="text-align: left;">Es wurde versucht, "%1! ls!" hinzuzufügen. Fehler: Es kann kein Dateisystem spezifischer eindeutiger Name für "%2! ls!" erstellt werden. -Dateisystem durchgeführt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl> <dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab118</dt> </dl></td>
<td style="text-align: left;">Das Element "%1! ls!" wurde nicht gefunden. in der filesystemimage-Hierarchie.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl> <dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab119</dt> </dl></td>
<td style="text-align: left;">Die Datei ' %1! s! ' in der filesystemimage-Hierarchie nicht gefunden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl> <dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab11a</dt> </dl></td>
<td style="text-align: left;">Das Verzeichnis "%1! s!". in der filesystemimage-Hierarchie nicht gefunden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl> <dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT) 0xc0aab120</dt> </dl></td>
<td style="text-align: left;">"%1! ls!" wird hinzugefügt. würde dazu führen, dass ein Ergebnisbild größer als das aktuell konfigurierte Limit ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl> <dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xc0aab121</dt> </dl></td>
<td style="text-align: left;">Der für die Eigenschaft "fremediablocks" angegebene Wert ist zu klein für die geschätzte Bild Größe basierend auf den aktuellen Daten. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl> <dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT) 0xc0aab200l</dt> </dl></td>
<td style="text-align: left;">Das Bild wird nicht an einer Sektorgrenze von 2 KB ausgerichtet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl> <dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab201l)</dt> </dl></td>
<td style="text-align: left;">Das Image enthält keinen gültigen volumedeskriptor.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl> <dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT) 0xc0aab202l</dt> </dl></td>
<td style="text-align: left;">Das Image wurde nicht mithilfe der <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>iisoimagemanager:: setpath</strong></a> -Methode oder der <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>iisoimagemanager:: setStream</strong></a> -Methode festgelegt, bevor die <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>iisoimagemanager:: Validate</strong></a> -Methode aufgerufen wurde.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl> <dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xc0aab203l</dt> </dl></td>
<td style="text-align: left;">Das angegebene Bild ist zu groß, um überprüft werden zu können, wenn die Größe <strong>MAXLONG</strong>überschreitet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl> <dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT) 0xc0aab128</dt> </dl></td>
<td style="text-align: left;">Der für die Datei "%1! ls!" angegebene Datenstrom. inkonsistent: erwartet: %2! I64d! bytes, gefunden: %3! I64d!. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl> <dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab129</dt> </dl></td>
<td style="text-align: left;">Es können keine Daten aus dem Stream für die Datei "%1! ls!" gelesen werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl> <dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab12a</dt> </dl></td>
<td style="text-align: left;">Fehler beim Erstellen des Datenstroms für die Datei "%1! ls!": <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl> <dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab12bl</dt> </dl></td>
<td style="text-align: left;">Fehler beim Aufzählen von Dateien in der Verzeichnisstruktur aufgrund von Berechtigungen nicht.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl> <dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT) 0xc0aab130</dt> </dl></td>
<td style="text-align: left;">Dieses Dateisystem Image enthält zu viele Verzeichnisse für "%1! ls!". -Dateisystem durchgeführt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl> <dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT) 0xc0aab131</dt> </dl></td>
<td style="text-align: left;">ISO9660 ist auf 8 Ebenen von Verzeichnissen beschränkt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl> <dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT) 0xc0aab132</dt> </dl></td>
<td style="text-align: left;">Die Datendatei ist zu groß für "%1! ls!". -Dateisystem durchgeführt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl> <dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab138</dt> </dl></td>
<td style="text-align: left;">%1! ls! kann nicht initialisiert werden. Stash-Datei.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl> <dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab139</dt> </dl></td>
<td style="text-align: left;">Fehler beim Suchen in "%1! ls!". Stash-Datei.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl> <dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab13a</dt> </dl></td>
<td style="text-align: left;">Fehler beim Schreiben in "%1! ls!". Stash-Datei.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl> <dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab13b</dt> </dl></td>
<td style="text-align: left;">Fehler beim Lesen von "%1! ls!". Stash-Datei.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl> <dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT) 0xc0aab140</dt> </dl></td>
<td style="text-align: left;">Das Arbeitsverzeichnis "%1! ls!" ist ungültig.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl> <dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT) 0xc0aab141</dt> </dl></td>
<td style="text-align: left;">Das Arbeitsverzeichnis kann nicht auf "%1! ls!" festgelegt werden. Verfügbarer Speicherplatz: %2! I64d! bytes, ungefähr %3! I64d! erforderliche bytes. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl> <dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT) 0xc0aab142</dt> </dl></td>
<td style="text-align: left;">Es wurde versucht, die Datenstapel Datei in das Verzeichnis "%1! ls!" zu verschieben. konnte nicht erfolgreich ausgeführt werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl> <dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT) 0xc0aab148</dt> </dl></td>
<td style="text-align: left;">Das Start Objekt konnte dem Bild nicht hinzugefügt werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl> <dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT) 0xc0aab149</dt> </dl></td>
<td style="text-align: left;">Ein Start Objekt kann nur in einem ersten Festplatten Abbild enthalten sein.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl> <dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT) 0xc0aab14a</dt> </dl></td>
<td style="text-align: left;">Der angeforderte Emulationstyp entspricht nicht der Größe des Start Abbilds.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl> <dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xc0aab150</dt> </dl></td>
<td style="text-align: left;">Optische Medien sind leer.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl> <dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xc0aab151</dt> </dl></td>
<td style="text-align: left;">Die angegebene Festplatte enthält keines der unterstützten Dateisysteme.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl> <dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab152</dt> </dl></td>
<td style="text-align: left;">Die angegebene Festplatte enthält kein "%1! ls!". -Dateisystem durchgeführt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl> <dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT) 0xc0aab153</dt> </dl></td>
<td style="text-align: left;">Beim Importieren von "%1! ls!" ist ein Konsistenz Fehler aufgetreten. -Dateisystem durchgeführt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl> <dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aab154</dt> </dl></td>
<td style="text-align: left;">"%1! ls!" das Dateisystem auf der ausgewählten CD enthält ein Feature, das für den Import nicht unterstützt wird: %2! ls!.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl> <dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT) 0xc0aab155</dt> </dl></td>
<td style="text-align: left;">"%2! ls!" konnte nicht importiert werden. Dateisystem von Disk. Die Datei "%1! ls!" ist bereits in der Bild Hierarchie als Verzeichnis vorhanden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl> <dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab156</dt> </dl></td>
<td style="text-align: left;">"%1" kann nicht durchsucht werden. I64d! auf der Quell-CD. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl> <dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab157</dt> </dl></td>
<td style="text-align: left;">Fehler beim Importieren aus vorheriger Sitzung aufgrund eines Fehlers beim Lesen eines Blocks auf dem Medium (wahrscheinlichste Block: %1! u!).<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl> <dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT) 0xc0aab158</dt> </dl></td>
<td style="text-align: left;">Der aktuelle Datenträger ist nicht der gleiche, von dem das Dateisystem importiert wurde.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl> <dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xc0aab159</dt> </dl></td>
<td style="text-align: left;">IMAPI lässt keine mehrfach Sitzung mit dem aktuellen Medientyp zu.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl> <dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT) 0xc0aab15a</dt> </dl></td>
<td style="text-align: left;">IMAPI kann nicht mehrere Sitzungen mit dem aktuellen Medium ausführen, da keine kompatible UDF-Revision zum Schreiben unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl> <dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xc0aab15b</dt> </dl></td>
<td style="text-align: left;">IMAPI unterstützt den angeforderten multisitzungstyp nicht.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl> <dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT) 0xc0aab133</dt> </dl></td>
<td style="text-align: left;">Fehler beim Vorgang aufgrund eines nicht kompatiblen Layouts der vorherigen Sitzung, die aus dem Medium importiert wurde.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl> <dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xc0aab15c</dt> </dl></td>
<td style="text-align: left;">IMAPI unterstützt keine der multisitzungstyp (e), die auf dem aktuellen Medium bereitgestellt werden.<br/>
<blockquote>
[!Note]<br />
[<strong>Ifilesystemimage:: ImportFile System</strong>] (/Windows/Desktop/API/IMAPI2FS/NF-IMAPI2FS-ifilesystemimage-importfilesystem)-Methode gibt diesen Fehler zurück, wenn das Aufzeichnungsgerät keine Medien enthält.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl> <dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT) 0xc0aab15d</dt> </dl></td>
<td style="text-align: left;">Die multisessioninterfaces-Eigenschaft muss festgelegt werden, bevor diese Methode aufgerufen wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl> <dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT) 0xc0aab15e</dt> </dl></td>
<td style="text-align: left;">"%2! ls!" konnte nicht importiert werden. Dateisystem von Disk. Das Verzeichnis "%1! ls!" ist in der Bild Hierarchie bereits als Datei vorhanden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl> <dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT) 0xc0aab162</dt> </dl></td>
<td style="text-align: left;">Einer der Parameter für mehrere Sitzungen kann nicht abgerufen werden oder weist einen falschen Wert auf.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl> <dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x00aab15fl</dt> </dl></td>
<td style="text-align: left;">Diese Funktion wird für die aktuelle Dateisystem Revision nicht unterstützt. Das Image wird ohne diese Funktion erstellt.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                                            |
| Header<br/>                   | <dl> <dt>Imapi2error. h; </dt> <dt>Imapi2fserror. h</dt> </dl> |



 

 





