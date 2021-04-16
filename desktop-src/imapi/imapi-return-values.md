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
# <a name="imapi-return-values"></a><span data-ttu-id="bd977-104">IMAPI-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bd977-104">IMAPI Return Values</span></span>

<span data-ttu-id="bd977-105">Die IMAPI-Methoden geben nicht negative Werte zurück (in der Regel ist dies \_ OK), wenn die Methode erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="bd977-105">The IMAPI methods return non-negative values, (typically S\_OK) if the method was successful.</span></span> <span data-ttu-id="bd977-106">Die IMAPI-Methoden geben Erfolgs-oder Fehlercodes von Winerror. h, Imapi2error. h oder Imapi2fserror. h bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="bd977-106">The IMAPI methods return success or error codes from Winerror.h, Imapi2error.h, or Imapi2fserror.h, on failure.</span></span>

<span data-ttu-id="bd977-107">Die folgenden Erfolgs-und Fehlercodes sind definiert.</span><span class="sxs-lookup"><span data-stu-id="bd977-107">The following success and error codes are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="bd977-108">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="bd977-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="bd977-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd977-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_BURN_VERIFICATION_FAILED"></span><span id="e_imapi_burn_verification_failed"></span><dl> <span data-ttu-id="bd977-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT) 0xc0aa0007l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-110"><dt><strong>E_IMAPI_BURN_VERIFICATION_FAILED</strong></dt> <dt>(HRESULT)0xC0AA0007L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-111">Der Datenträger hat die Überprüfung der Überprüfung nicht bestanden und kann beschädigte Daten enthalten oder nicht verwendbar sein.</span><span class="sxs-lookup"><span data-stu-id="bd977-111">The disc did not pass burn verification and may contain corrupt data or be unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_REQUEST_CANCELLED"></span><span id="e_imapi_request_cancelled"></span><dl> <span data-ttu-id="bd977-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT) 0xc0aa0002</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-112"><dt><strong>E_IMAPI_REQUEST_CANCELLED</strong></dt> <dt>(HRESULT)0xC0AA0002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-113">Die Anforderung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="bd977-113">The request was canceled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_REQUIRED"></span><span id="e_imapi_recorder_required"></span><dl> <span data-ttu-id="bd977-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT) 0xc0aa0003</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-114"><dt><strong>E_IMAPI_RECORDER_REQUIRED</strong></dt> <dt>(HRESULT)0xC0AA0003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-115">Für die Anforderung muss eine aktuelle Disc Recorder ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-115">The request requires a current disc recorder to be selected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_WRITE_NOT_IN_PROGRESS"></span><span id="s_imapi_write_not_in_progress"></span><dl> <span data-ttu-id="bd977-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0x00aa0302l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-116"><dt><strong>S_IMAPI_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0x00AA0302L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-117">Zurzeit wird kein Schreibvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-117">No write operation is currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_SPEEDADJUSTED"></span><span id="s_imapi_speedadjusted"></span><dl> <span data-ttu-id="bd977-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT) 0x00aa0004</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-118"><dt><strong>S_IMAPI_SPEEDADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-119">Die angeforderte Schreibgeschwindigkeit wurde vom Laufwerk nicht unterstützt, und die Geschwindigkeit wurde angepasst.</span><span class="sxs-lookup"><span data-stu-id="bd977-119">The requested write speed was not supported by the drive and the speed was adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_ROTATIONADJUSTED"></span><span id="s_imapi_rotationadjusted"></span><dl> <span data-ttu-id="bd977-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT) 0x00aa0005</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-120"><dt><strong>S_IMAPI_ROTATIONADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-121">Der angeforderte drehungstyp wurde vom Laufwerk nicht unterstützt, und der drehtyp wurde angepasst.</span><span class="sxs-lookup"><span data-stu-id="bd977-121">The requested rotation type was not supported by the drive and the rotation type was adjusted.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_BOTHADJUSTED"></span><span id="s_imapi_bothadjusted"></span><dl> <span data-ttu-id="bd977-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT) 0x00aa0006</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-122"><dt><strong>S_IMAPI_BOTHADJUSTED</strong></dt> <dt>(HRESULT)0x00AA0006</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-123">Die angeforderte Schreibgeschwindigkeit und der drehtyp wurden vom Laufwerk nicht unterstützt, und beide wurden angepasst.</span><span class="sxs-lookup"><span data-stu-id="bd977-123">The requested write speed and rotation type were not supported by the drive and they were both adjusted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="S_IMAPI_COMMAND_HAS_SENSE_DATA"></span><span id="s_imapi_command_has_sense_data"></span><dl> <span data-ttu-id="bd977-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT) 0x00aa0200</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-124"><dt><strong>S_IMAPI_COMMAND_HAS_SENSE_DATA</strong></dt> <dt>(HRESULT)0x00AA0200</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-125">Das Gerät hat den Befehl akzeptiert, hat jedoch die Sense-Daten zurückgegeben, die auf einen Fehler hinweisen.</span><span class="sxs-lookup"><span data-stu-id="bd977-125">The device accepted the command, but returned sense data, indicating an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_IS_READ_ONLY"></span><span id="e_imapi_raw_image_is_read_only"></span><dl> <span data-ttu-id="bd977-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT) 0x80aa0a00l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-126"><dt><strong>E_IMAPI_RAW_IMAGE_IS_READ_ONLY</strong></dt> <dt>(HRESULT)0x80AA0A00L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-127">Das Image ist aufgrund eines Aufrufes durch einen Aufrufen von <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>irawcdimagecreator:: kreateresultimage</strong></a>schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-127">The image has become read-only due to a call to <a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage"><strong>IRawCDImageCreator::CreateResultImage</strong></a>.</span></span> <span data-ttu-id="bd977-128">Daher kann das Objekt nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-128">As a result the object can no longer be modified.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS"></span><span id="e_imapi_raw_image_too_many_tracks"></span><dl> <span data-ttu-id="bd977-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT) 0x80aa0a01l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-129"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A01L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-130">Es können keine weiteren Spuren hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-130">No more tracks may be added.</span></span> <span data-ttu-id="bd977-131">CD-Medien sind auf einen Bereich von 1-99-Spuren beschränkt.</span><span class="sxs-lookup"><span data-stu-id="bd977-131">CD media is restricted to a range of 1-99 tracks.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_NO_TRACKS"></span><span id="e_imapi_raw_image_no_tracks"></span><dl> <span data-ttu-id="bd977-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT) 0x80aa0a03l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-132"><dt><strong>E_IMAPI_RAW_IMAGE_NO_TRACKS</strong></dt> <dt>(HRESULT)0x80AA0A03L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-133">Vor der Verwendung dieser Funktion müssen dem bildspuren hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-133">Tracks must be added to the image before using this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_raw_image_sector_type_not_supported"></span><dl> <span data-ttu-id="bd977-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80aa0a02l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-134"><dt><strong>E_IMAPI_RAW_IMAGE_SECTOR_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0A02L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-135">Der angeforderte sektortyp wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-135">The requested sector type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED"></span><span id="e_imapi_raw_image_tracks_already_added"></span><dl> <span data-ttu-id="bd977-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT) 0x80aa0a04l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-136"><dt><strong>E_IMAPI_RAW_IMAGE_TRACKS_ALREADY_ADDED</strong></dt> <dt>(HRESULT)0x80AA0A04L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-137">Vor der Verwendung dieser Funktion können dem Bild keine Spuren hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-137">Tracks may not be added to the image prior to the use of this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE"></span><span id="e_imapi_raw_image_insufficient_space"></span><dl> <span data-ttu-id="bd977-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT) 0x80aa0a05l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-138"><dt><strong>E_IMAPI_RAW_IMAGE_INSUFFICIENT_SPACE</strong></dt> <dt>(HRESULT)0x80AA0A05L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-139">Durch das Hinzufügen dieses Titels würden die Einschränkungen des Starts der Leadout-Eigenschaft überschritten.</span><span class="sxs-lookup"><span data-stu-id="bd977-139">Adding this track would exceed the limitations of the start of the leadout.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES"></span><span id="e_imapi_raw_image_too_many_track_indexes"></span><dl> <span data-ttu-id="bd977-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT) 0x80aa0a06l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-140"><dt><strong>E_IMAPI_RAW_IMAGE_TOO_MANY_TRACK_INDEXES</strong></dt> <dt>(HRESULT)0x80AA0A06L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-141">Durch das Hinzufügen dieses Titels würde die Index Grenze von 99 überschritten.</span><span class="sxs-lookup"><span data-stu-id="bd977-141">Adding this track would exceed the 99 index limit.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND"></span><span id="e_imapi_raw_image_track_index_not_found"></span><dl> <span data-ttu-id="bd977-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT) 0x80aa0a07l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-142"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_NOT_FOUND</strong></dt> <dt>(HRESULT)0x80AA0A07L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-143">Der angegebene LBA-Offset ist nicht in der Liste der Nachverfolgung-Indizes enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd977-143">The specified LBA offset is not in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS"></span><span id="s_imapi_raw_image_track_index_already_exists"></span><dl> <span data-ttu-id="bd977-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT) 0x00aa0a08l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-144"><dt><strong>S_IMAPI_RAW_IMAGE_TRACK_INDEX_ALREADY_EXISTS</strong></dt> <dt>(HRESULT)0x00AA0A08L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-145">Der angegebene LBA-Offset befindet sich bereits in der Liste der Nachverfolgung-Indizes.</span><span class="sxs-lookup"><span data-stu-id="bd977-145">The specified LBA offset is already in the list of track indexes.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED"></span><span id="e_imapi_raw_image_track_index_offset_zero_cannot_be_cleared"></span><dl> <span data-ttu-id="bd977-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT) 0x80aa0a09l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-146"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_OFFSET_ZERO_CANNOT_BE_CLEARED</strong></dt> <dt>(HRESULT)0x80AA0A09L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-147">Der Index 1 (LBA-Offset NULL) kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-147">Index 1 (LBA offset zero) cannot be cleared.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX"></span><span id="e_imapi_raw_image_track_index_too_close_to_other_index"></span><dl> <span data-ttu-id="bd977-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT) 0x80aa0a0al</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-148"><dt><strong>E_IMAPI_RAW_IMAGE_TRACK_INDEX_TOO_CLOSE_TO_OTHER_INDEX</strong></dt> <dt>(HRESULT)0x80AA0A0AL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-149">Jeder Index muss über eine minimale Größe von zehn Sektoren verfügen.</span><span class="sxs-lookup"><span data-stu-id="bd977-149">Each index must have a minimum size of ten sectors.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE"></span><span id="e_imapi_recorder_no_such_mode_page"></span><dl> <span data-ttu-id="bd977-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT) 0xc0aa0201</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-150"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</strong></dt> <dt>(HRESULT)0xC0AA0201</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-151">Das Gerät hat gemeldet, dass die Seite angeforderter Modus (und Typ) nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bd977-151">The device reported that the requested mode page (and type) is not present.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_NO_MEDIA"></span><span id="e_imapi_recorder_media_no_media"></span><dl> <span data-ttu-id="bd977-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT) 0xc0aa0202</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-152"><dt><strong>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0202</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-153">Es ist kein Medium auf dem Gerät vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bd977-153">There is no media in the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE"></span><span id="e_imapi_recorder_media_incompatible"></span><dl> <span data-ttu-id="bd977-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT) 0xc0aa0203</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-154"><dt><strong>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AA0203</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-155">Das Medium ist nicht kompatibel oder weist ein unbekanntes physisches Format auf.</span><span class="sxs-lookup"><span data-stu-id="bd977-155">The media is not compatible or of unknown physical format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN"></span><span id="e_imapi_recorder_media_upside_down"></span><dl> <span data-ttu-id="bd977-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT) 0xc0aa0204</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-156"><dt><strong>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</strong></dt> <dt>(HRESULT)0xC0AA0204</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-157">Das Medium wird nach oben eingefügt.</span><span class="sxs-lookup"><span data-stu-id="bd977-157">The media is inserted upside down.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BECOMING_READY"></span><span id="e_imapi_recorder_media_becoming_ready"></span><dl> <span data-ttu-id="bd977-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT) 0xc0aa0205</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-158"><dt><strong>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</strong></dt> <dt>(HRESULT)0xC0AA0205</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-159">Das Laufwerk hat gemeldet, dass es gerade bereit ist.</span><span class="sxs-lookup"><span data-stu-id="bd977-159">The drive reported that it is in the process of becoming ready.</span></span> <span data-ttu-id="bd977-160">Wiederholen Sie die Anforderung später.</span><span class="sxs-lookup"><span data-stu-id="bd977-160">Please try the request again later.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS"></span><span id="e_imapi_recorder_media_format_in_progress"></span><dl> <span data-ttu-id="bd977-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0206</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-161"><dt><strong>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0206</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-162">Das Medium wird zurzeit formatiert.</span><span class="sxs-lookup"><span data-stu-id="bd977-162">The media is currently being formatted.</span></span> <span data-ttu-id="bd977-163">Warten Sie, bis das Format fertiggestellt wurde, bevor Sie versuchen, die Medien zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bd977-163">Please wait for the format to complete before attempting to use the media.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_BUSY"></span><span id="e_imapi_recorder_media_busy"></span><dl> <span data-ttu-id="bd977-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT) 0xc0aa0207</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-164"><dt><strong>E_IMAPI_RECORDER_MEDIA_BUSY</strong></dt> <dt>(HRESULT)0xC0AA0207</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-165">Das Laufwerk hat gemeldet, dass es einen Vorgang mit langer Laufzeit ausführt, z. b. das Abschließen eines Schreibvorgangs.</span><span class="sxs-lookup"><span data-stu-id="bd977-165">The drive reported that it is performing a long-running operation, such as finishing a write.</span></span> <span data-ttu-id="bd977-166">Das Laufwerk ist möglicherweise für längere Zeit unbrauchbar.</span><span class="sxs-lookup"><span data-stu-id="bd977-166">The drive may be unusable for a long period of time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS"></span><span id="e_imapi_recorder_invalid_mode_parameters"></span><dl> <span data-ttu-id="bd977-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT) 0xc0aa0208</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-167"><dt><strong>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</strong></dt> <dt>(HRESULT)0xC0AA0208</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-168">Das Laufwerk hat gemeldet, dass die Kombination der Parameter, die auf der Seite Modus für einen Modus SELECT-Befehl angegeben wurde, nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="bd977-168">The drive reported that the combination of parameters provided in the mode page for a MODE SELECT command were not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED"></span><span id="e_imapi_recorder_media_write_protected"></span><dl> <span data-ttu-id="bd977-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT) 0xc0aa0209</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-169"><dt><strong>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</strong></dt> <dt>(HRESULT)0xC0AA0209</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-170">Das Laufwerk hat gemeldet, dass das Medium schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="bd977-170">The drive reported that the media is write protected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_NO_SUCH_FEATURE"></span><span id="e_imapi_recorder_no_such_feature"></span><dl> <span data-ttu-id="bd977-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT) 0xc0aa020a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-171"><dt><strong>E_IMAPI_RECORDER_NO_SUCH_FEATURE</strong></dt> <dt>(HRESULT)0xC0AA020A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-172">Die angeforderte funktionsseite wird vom Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-172">The feature page requested is not supported by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT"></span><span id="e_imapi_recorder_feature_is_not_current"></span><dl> <span data-ttu-id="bd977-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT) 0xc0aa020b</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-173"><dt><strong>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</strong></dt> <dt>(HRESULT)0xC0AA020B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-174">Die angeforderte funktionsseite wird unterstützt, aber nicht als aktuell gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bd977-174">The feature page requested is supported, but is not marked as current.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED"></span><span id="e_imapi_recorder_get_configuration_not_supported"></span><dl> <span data-ttu-id="bd977-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa020c</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-175"><dt><strong>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA020C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-176">Der Befehl "Get Configuration" wird vom Laufwerk nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-176">The drive does not support the GET CONFIGURATION command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_COMMAND_TIMEOUT"></span><span id="e_imapi_recorder_command_timeout"></span><dl> <span data-ttu-id="bd977-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT) 0xc0aa020d</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-177"><dt><strong>E_IMAPI_RECORDER_COMMAND_TIMEOUT</strong></dt> <dt>(HRESULT)0xC0AA020D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-178">Das Gerät konnte den Befehl innerhalb des Timeout Zeitraums nicht akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="bd977-178">The device failed to accept the command within the timeout period.</span></span> <span data-ttu-id="bd977-179">Dies kann darauf zurückzuführen sein, dass das Gerät in einen inkonsistenten Status eingetreten ist, oder dass der Timeout Wert für den Befehl möglicherweise gesteigert werden muss.</span><span class="sxs-lookup"><span data-stu-id="bd977-179">This may be caused by the device having entered an inconsistent state, or the timeout value for the command may need to be increased.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT"></span><span id="e_imapi_recorder_dvd_structure_not_present"></span><dl> <span data-ttu-id="bd977-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT) 0xc0aa020E</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-180"><dt><strong>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</strong></dt> <dt>(HRESULT)0xC0AA020E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-181">Die DVD-Struktur ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bd977-181">The DVD structure is not present.</span></span> <span data-ttu-id="bd977-182">Dies kann durch nicht verwendetes nicht verwendetes Laufwerk/Medium verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-182">This may be caused by incompatible drive/medium used.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH"></span><span id="e_imapi_recorder_media_speed_mismatch"></span><dl> <span data-ttu-id="bd977-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT) 0xc0aa020f</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-183"><dt><strong>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AA020F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-184">Die Geschwindigkeit des Mediums ist mit dem Gerät nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="bd977-184">The media's speed is incompatible with the device.</span></span> <span data-ttu-id="bd977-185">Dies kann durch die Verwendung eines höheren oder niedrigeren Geschwindigkeits Mediums verursacht werden, als der vom Gerät unterstützte Bereich von Geschwindigkeiten.</span><span class="sxs-lookup"><span data-stu-id="bd977-185">This may be caused by using higher or lower speed media than the range of speeds supported by the device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_LOCKED"></span><span id="e_imapi_recorder_locked"></span><dl> <span data-ttu-id="bd977-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT) 0xc0aa0210</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-186"><dt><strong>E_IMAPI_RECORDER_LOCKED</strong></dt> <dt>(HRESULT)0xC0AA0210</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-187">Das Gerät, das dieser Aufzeichnung während des letzten Vorgangs zugeordnet ist, wurde exklusiv gesperrt und führt zu einem Fehler bei diesem Vorgang.</span><span class="sxs-lookup"><span data-stu-id="bd977-187">The device associated with this recorder during the last operation has been exclusively locked, causing this operation to fail.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_recorder_client_name_is_not_valid"></span><dl> <span data-ttu-id="bd977-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa0211</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-188"><dt><strong>E_IMAPI_RECORDER_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0211</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-189">Der Client Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-189">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_recorder_invalid_response_from_device"></span><dl> <span data-ttu-id="bd977-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xc0aa02ff</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-190"><dt><strong>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA02FF</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-191">Das Gerät meldete unerwartete oder ungültige Daten für einen Befehl.</span><span class="sxs-lookup"><span data-stu-id="bd977-191">The device reported unexpected or invalid data for a command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_LOSS_OF_STREAMING"></span><span id="e_imapi_loss_of_streaming"></span><dl> <span data-ttu-id="bd977-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT) 0xc0aa0300</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-192"><dt><strong>E_IMAPI_LOSS_OF_STREAMING</strong></dt> <dt>(HRESULT)0xC0AA0300</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-193">Der Schreibvorgang ist fehlgeschlagen, da das Laufwerk keine Daten schnell genug empfangen hat, um das Schreiben fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="bd977-193">The write failed because the drive did not receive data quickly enough to continue writing.</span></span> <span data-ttu-id="bd977-194">Wenn Sie die Quelldaten auf den lokalen Computer verschieben, die Schreibgeschwindigkeit reduzieren oder eine &quot; Einstellung für einen Pufferunterlauf freigeben, &quot; kann dieses Problem möglicherweise behoben werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-194">Moving the source data to the local computer, reducing the write speed, or enabling a &quot;buffer underrun free&quot; setting may resolve this issue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE"></span><span id="e_imapi_unexpected_response_from_device"></span><dl> <span data-ttu-id="bd977-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT) 0xc0aa0301</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-195"><dt><strong>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</strong></dt> <dt>(HRESULT)0xC0AA0301</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-196">Das Schreiben ist fehlgeschlagen, weil das Laufwerk Fehlerinformationen zurückgegeben hat, die nicht von wieder hergestellt werden konnten.</span><span class="sxs-lookup"><span data-stu-id="bd977-196">The write failed because the drive returned error information that could not be recovered from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2data_write_in_progress"></span><dl> <span data-ttu-id="bd977-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0400</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-197"><dt><strong>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0400</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-198">Zurzeit wird ein Schreibvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-198">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2data_write_not_in_progress"></span><dl> <span data-ttu-id="bd977-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0401</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-199"><dt><strong>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0401</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-200">Zurzeit wird kein Schreibvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-200">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_INVALID_MEDIA_STATE"></span><span id="e_imapi_df2data_invalid_media_state"></span><dl> <span data-ttu-id="bd977-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT) 0xc0aa0402</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-201"><dt><strong>E_IMAPI_DF2DATA_INVALID_MEDIA_STATE</strong></dt> <dt>(HRESULT)0xC0AA0402</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-202">Der angeforderte Vorgang ist nur mit unterstützten Medien gültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-202">The requested operation is only valid with supported media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2data_stream_not_supported"></span><dl> <span data-ttu-id="bd977-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0403</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-203"><dt><strong>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0403</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-204">Der bereitgestellte zu schreibende Datenstrom wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-204">The provided stream to write is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA"></span><span id="e_imapi_df2data_stream_too_large_for_current_media"></span><dl> <span data-ttu-id="bd977-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT) 0xc0aa0404</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-205"><dt><strong>E_IMAPI_DF2DATA_STREAM_TOO_LARGE_FOR_CURRENT_MEDIA</strong></dt> <dt>(HRESULT)0xC0AA0404</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-206">Der bereitgestellte zu schreibende Stream ist zu groß für die aktuell eingefügten Medien.</span><span class="sxs-lookup"><span data-stu-id="bd977-206">The provided stream to write is too large for the currently inserted media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_NOT_BLANK"></span><span id="e_imapi_df2data_media_not_blank"></span><dl> <span data-ttu-id="bd977-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xc0aa0405</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-207"><dt><strong>E_IMAPI_DF2DATA_MEDIA_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0405</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-208">Das Überschreiben von nicht leeren Medien ist nicht zulässig, ohne dass die Eigenschaft forceüberschreibung auf VARIANT_TRUE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bd977-208">Overwriting non-blank media is not allowed without the ForceOverwrite property set to VARIANT_TRUE.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2data_media_is_not_supported"></span><dl> <span data-ttu-id="bd977-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0406</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-209"><dt><strong>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0406</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-210">Der aktuelle Medientyp wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-210">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2data_recorder_not_supported"></span><dl> <span data-ttu-id="bd977-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0407</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-211"><dt><strong>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0407</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-212">Dieses Gerät unterstützt nicht die Vorgänge, die für dieses Festplatten Format erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bd977-212">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2data_client_name_is_not_valid"></span><dl> <span data-ttu-id="bd977-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa0408</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-213"><dt><strong>E_IMAPI_DF2DATA_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0408</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-214">Der Client Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-214">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_in_progress"></span><dl> <span data-ttu-id="bd977-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0500</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-215"><dt><strong>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0500</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-216">Zurzeit wird ein Schreibvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-216">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2tao_write_not_in_progress"></span><dl> <span data-ttu-id="bd977-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0501</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-217"><dt><strong>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0501</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-218">Zurzeit wird kein Schreibvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-218">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2tao_media_is_not_prepared"></span><dl> <span data-ttu-id="bd977-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xc0aa0502</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-219"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0502</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-220">Der angeforderte Vorgang ist nur gültig, wenn Medien &quot; vorbereitet wurden &quot; .</span><span class="sxs-lookup"><span data-stu-id="bd977-220">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2tao_media_is_prepared"></span><dl> <span data-ttu-id="bd977-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xc0aa0503</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-221"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0503</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-222">Der angeforderte Vorgang ist ungültig, wenn Medien &quot; vorbereitet, &quot; aber nicht freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="bd977-222">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY"></span><span id="e_imapi_df2tao_property_for_blank_media_only"></span><dl> <span data-ttu-id="bd977-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT) 0xc0aa0504</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-223"><dt><strong>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</strong></dt> <dt>(HRESULT)0xC0AA0504</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-224">Die-Eigenschaft kann nicht geändert werden, nachdem auf das Medium geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="bd977-224">The property cannot be changed once the media has been written to.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC"></span><span id="e_imapi_df2tao_table_of_contents_empty_disc"></span><dl> <span data-ttu-id="bd977-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xc0aa0505</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-225"><dt><strong>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AA0505</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-226">Das Inhaltsverzeichnis kann nicht von einem leeren Laufwerk abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-226">The table of contents cannot be retrieved from an empty disc.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2tao_media_is_not_blank"></span><dl> <span data-ttu-id="bd977-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xc0aa0506</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-227"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0506</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-228">Es werden nur leere CD-R/RW-Medien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-228">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_media_is_not_supported"></span><dl> <span data-ttu-id="bd977-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0507</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-229"><dt><strong>E_IMAPI_DF2TAO_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0507</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-230">Es werden nur leere CD-R/RW-Medien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-230">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED"></span><span id="e_imapi_df2tao_track_limit_reached"></span><dl> <span data-ttu-id="bd977-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT) 0xc0aa0508</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-231"><dt><strong>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</strong></dt> <dt>(HRESULT)0xC0AA0508</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-232">CD-R-und CD-RW-Medien unterstützen maximal 99 Audiospuren.</span><span class="sxs-lookup"><span data-stu-id="bd977-232">CD-R and CD-RW media support a maximum of 99 audio tracks.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2tao_not_enough_space"></span><dl> <span data-ttu-id="bd977-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xc0aa0509</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-233"><dt><strong>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0509</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-234">Auf dem Medium ist nicht genügend Speicherplatz vorhanden, um die bereitgestellte Audiospur hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bd977-234">There is not enough space left on the media to add the provided audio track.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2tao_no_recorder_specified"></span><dl> <span data-ttu-id="bd977-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xc0aa050a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-235"><dt><strong>E_IMAPI_DF2TAO_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA050A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-236">Sie können das Medium erst vorbereiten, nachdem Sie eine Aufzeichnung ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="bd977-236">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_ISRC"></span><span id="e_imapi_df2tao_invalid_isrc"></span><dl> <span data-ttu-id="bd977-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT) 0xc0aa050b</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-237"><dt><strong>E_IMAPI_DF2TAO_INVALID_ISRC</strong></dt> <dt>(HRESULT)0xC0AA050B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-238">Der angegebene ISRC-Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-238">The ISRC provided is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_INVALID_MCN"></span><span id="e_imapi_df2tao_invalid_mcn"></span><dl> <span data-ttu-id="bd977-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT) 0xc0aa050c</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-239"><dt><strong>E_IMAPI_DF2TAO_INVALID_MCN</strong></dt> <dt>(HRESULT)0xC0AA050C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-240">Die angegebene Medienkatalog Nummer ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-240">The Media Catalog Number provided is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_stream_not_supported"></span><dl> <span data-ttu-id="bd977-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa050d</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-241"><dt><strong>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-242">Der bereitgestellte Audiodatenstrom ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-242">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2tao_recorder_not_supported"></span><dl> <span data-ttu-id="bd977-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa050E</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-243"><dt><strong>E_IMAPI_DF2TAO_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA050E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-244">Dieses Gerät unterstützt nicht die Vorgänge, die für dieses Festplatten Format erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bd977-244">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2tao_client_name_is_not_valid"></span><dl> <span data-ttu-id="bd977-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa050f</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-245"><dt><strong>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA050F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-246">Der Client Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-246">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_in_progress"></span><dl> <span data-ttu-id="bd977-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0600</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-247"><dt><strong>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0600</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-248">Zurzeit wird ein Schreibvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-248">There is currently a write operation in progress.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS"></span><span id="e_imapi_df2raw_write_not_in_progress"></span><dl> <span data-ttu-id="bd977-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT) 0xc0aa0601</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-249"><dt><strong>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</strong></dt> <dt>(HRESULT)0xC0AA0601</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-250">Zurzeit wird kein Schreibvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-250">There is no write operation currently in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED"></span><span id="e_imapi_df2raw_media_is_not_prepared"></span><dl> <span data-ttu-id="bd977-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT) 0xc0aa0602</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-251"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0602</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-252">Der angeforderte Vorgang ist nur gültig, wenn Medien &quot; vorbereitet wurden &quot; .</span><span class="sxs-lookup"><span data-stu-id="bd977-252">The requested operation is only valid when media has been &quot;prepared&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_PREPARED"></span><span id="e_imapi_df2raw_media_is_prepared"></span><dl> <span data-ttu-id="bd977-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT) 0xc0aa0603</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-253"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_PREPARED</strong></dt> <dt>(HRESULT)0xC0AA0603</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-254">Der angeforderte Vorgang ist ungültig, wenn Medien &quot; vorbereitet, &quot; aber nicht freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="bd977-254">The requested operation is not valid when media has been &quot;prepared&quot; but not released.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_df2raw_client_name_is_not_valid"></span><dl> <span data-ttu-id="bd977-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa0604</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-255"><dt><strong>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA0604</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-256">Der Client Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-256">The client name is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK"></span><span id="e_imapi_df2raw_media_is_not_blank"></span><dl> <span data-ttu-id="bd977-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT) 0xc0aa0606</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-257"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</strong></dt> <dt>(HRESULT)0xC0AA0606</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-258">Es werden nur leere CD-R/RW-Medien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-258">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_media_is_not_supported"></span><dl> <span data-ttu-id="bd977-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0607</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-259"><dt><strong>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0607</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-260">Es werden nur leere CD-R/RW-Medien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-260">Only blank CD-R/RW media is supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE"></span><span id="e_imapi_df2raw_not_enough_space"></span><dl> <span data-ttu-id="bd977-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT) 0xc0aa0609</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-261"><dt><strong>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</strong></dt> <dt>(HRESULT)0xC0AA0609</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-262">Es ist nicht genügend Speicherplatz auf dem Medium vorhanden, um die angegebene Sitzung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bd977-262">There is not enough space on the media to add the provided session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED"></span><span id="e_imapi_df2raw_no_recorder_specified"></span><dl> <span data-ttu-id="bd977-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT) 0xc0aa060a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-263"><dt><strong>E_IMAPI_DF2RAW_NO_RECORDER_SPECIFIED</strong></dt> <dt>(HRESULT)0xC0AA060A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-264">Sie können das Medium erst vorbereiten, nachdem Sie eine Aufzeichnung ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="bd977-264">You cannot prepare the media until you choose a recorder to use.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_stream_not_supported"></span><dl> <span data-ttu-id="bd977-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa060d</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-265"><dt><strong>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-266">Der bereitgestellte Audiodatenstrom ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-266">The provided audio stream is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_data_block_type_not_supported"></span><dl> <span data-ttu-id="bd977-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa060E</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-267"><dt><strong>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA060E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-268">Der angeforderte Daten Blocktyp wird vom aktuellen Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-268">The requested data block type is not supported by the current device.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT"></span><span id="e_imapi_df2raw_stream_leadin_too_short"></span><dl> <span data-ttu-id="bd977-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT) 0xc0aa060f</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-269"><dt><strong>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</strong></dt> <dt>(HRESULT)0xC0AA060F</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-270">Der Stream enthält keine ausreichende Anzahl von Sektoren im Leadin für das aktuelle Medium.</span><span class="sxs-lookup"><span data-stu-id="bd977-270">The stream does not contain a sufficient number of sectors in the leadin for the current media.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_df2raw_recorder_not_supported"></span><dl> <span data-ttu-id="bd977-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0610</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-271"><dt><strong>E_IMAPI_DF2RAW_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0610</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-272">Dieses Gerät unterstützt nicht die Vorgänge, die für dieses Festplatten Format erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bd977-272">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_IN_USE"></span><span id="e_imapi_erase_recorder_in_use"></span><dl> <span data-ttu-id="bd977-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT) 0x80aa0900</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-273"><dt><strong>E_IMAPI_ERASE_RECORDER_IN_USE</strong></dt> <dt>(HRESULT)0x80AA0900</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-274">Das Format verwendet derzeit den Disk Recorder für einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="bd977-274">The format is currently using the disc recorder for an erase operation.</span></span> <span data-ttu-id="bd977-275">Warten Sie, bis der Löschvorgang beendet ist, bevor Sie versuchen, den aktuellen Disk Recorder festzulegen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="bd977-275">Please wait for the erase to complete before attempting to set or clear the current disc recorder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED"></span><span id="e_imapi_erase_only_one_recorder_supported"></span><dl> <span data-ttu-id="bd977-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT) 0x80aa0901</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-276"><dt><strong>E_IMAPI_ERASE_ONLY_ONE_RECORDER_SUPPORTED</strong></dt> <dt>(HRESULT)0x80AA0901</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-277">Das Lösch Format unterstützt nur eine Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="bd977-277">The erase format only supports one recorder.</span></span> <span data-ttu-id="bd977-278">Sie müssen den aktuellen Recorder löschen, bevor Sie einen neuen festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="bd977-278">You must clear the current recorder before setting a new one.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL"></span><span id="e_imapi_erase_disc_information_too_small"></span><dl> <span data-ttu-id="bd977-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80aa0902</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-279"><dt><strong>E_IMAPI_ERASE_DISC_INFORMATION_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0902</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-280">Das Laufwerk hat nicht genügend Daten für einen Befehl zum Lesen von Festplatten Informationen gemeldet.</span><span class="sxs-lookup"><span data-stu-id="bd977-280">The drive did not report sufficient data for a READ DISC INFORMATION command.</span></span> <span data-ttu-id="bd977-281">Das Laufwerk wird möglicherweise nicht unterstützt, oder die Medien sind möglicherweise nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="bd977-281">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL"></span><span id="e_imapi_erase_mode_page_2a_too_small"></span><dl> <span data-ttu-id="bd977-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT) 0x80aa0903</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-282"><dt><strong>E_IMAPI_ERASE_MODE_PAGE_2A_TOO_SMALL</strong></dt> <dt>(HRESULT)0x80AA0903</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-283">Das Laufwerk hat nicht genügend Daten für einen modussense-Befehl (Page 0x2A) gemeldet.</span><span class="sxs-lookup"><span data-stu-id="bd977-283">The drive did not report sufficient data for a MODE SENSE (page 0x2A) command.</span></span> <span data-ttu-id="bd977-284">Das Laufwerk wird möglicherweise nicht unterstützt, oder die Medien sind möglicherweise nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="bd977-284">The drive may not be supported, or the media may not be correct.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE"></span><span id="e_imapi_erase_media_is_not_erasable"></span><dl> <span data-ttu-id="bd977-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT) 0x80aa0904</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-285"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_ERASABLE</strong></dt> <dt>(HRESULT)0x80AA0904</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-286">Das Laufwerk hat gemeldet, dass das Medium nicht Lösch fähig ist.</span><span class="sxs-lookup"><span data-stu-id="bd977-286">The drive reported that the media is not erasable.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND"></span><span id="e_imapi_erase_drive_failed_erase_command"></span><dl> <span data-ttu-id="bd977-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT) 0x80aa0905</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-287"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_ERASE_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0905</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-288">Der Löschbefehl des Laufwerks ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="bd977-288">The drive failed the erase command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR"></span><span id="e_imapi_erase_took_longer_than_one_hour"></span><dl> <span data-ttu-id="bd977-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT) 0x80aa0906</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-289"><dt><strong>E_IMAPI_ERASE_TOOK_LONGER_THAN_ONE_HOUR</strong></dt> <dt>(HRESULT)0x80AA0906</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-290">Das Laufwerk hat das Löschen innerhalb einer Stunde nicht vervollständigt.</span><span class="sxs-lookup"><span data-stu-id="bd977-290">The drive did not complete the erase in one hour.</span></span> <span data-ttu-id="bd977-291">Für das Laufwerk ist möglicherweise ein Energie-und Entfernungs Vorgang oder ein anderer manueller Eingriff erforderlich, um den ordnungsgemäßen Betrieb fortzusetzen</span><span class="sxs-lookup"><span data-stu-id="bd977-291">The drive may require a power cycle, media removal, or other manual intervention to resume proper operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bd977-292">Dieser Wert wird derzeit auch zurückgegeben, wenn der Versuch, ein Löschvorgang auf CD-RW-oder DVD-RW-Medien über die <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> -Schnittstelle durchzuführen, aufgrund eines ungültigen Mediums fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="bd977-292">Currently, this value will also be returned if an attempt to perform an erase on CD-RW or DVD-RW media via the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a> interface fails as a result of the media being bad.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE"></span><span id="e_imapi_erase_unexpected_drive_response_during_erase"></span><dl> <span data-ttu-id="bd977-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT) 0x80aa0907</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-293"><dt><strong>E_IMAPI_ERASE_UNEXPECTED_DRIVE_RESPONSE_DURING_ERASE</strong></dt> <dt>(HRESULT)0x80AA0907</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-294">Das Laufwerk hat während des Löschvorgangs einen unerwarteten Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd977-294">The drive returned an unexpected error during the erase.</span></span> <span data-ttu-id="bd977-295">Möglicherweise sind die Medien nicht verwendbar, der Löschvorgang ist möglicherweise noch nicht möglich, oder das Laufwerk ist dabei, die Festplatte zu löschen.</span><span class="sxs-lookup"><span data-stu-id="bd977-295">The media may be unusable, the erase may be complete, or the drive may still be in the process of erasing the disc.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND"></span><span id="e_imapi_erase_drive_failed_spinup_command"></span><dl> <span data-ttu-id="bd977-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT) 0x80aa0908</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-296"><dt><strong>E_IMAPI_ERASE_DRIVE_FAILED_SPINUP_COMMAND</strong></dt> <dt>(HRESULT)0x80AA0908</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-297">Das Laufwerk hat einen Fehler für einen Start Unit (SpinUp)-Befehl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd977-297">The drive returned an error for a START UNIT (spinup) command.</span></span> <span data-ttu-id="bd977-298">Möglicherweise ist ein manueller Eingriff erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bd977-298">Manual intervention may be required.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED"></span><span id="e_imapi_erase_media_is_not_supported"></span><dl> <span data-ttu-id="bd977-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa0909</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-299"><dt><strong>E_IMAPI_ERASE_MEDIA_IS_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA0909</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-300">Der aktuelle Medientyp wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-300">The current media type is unsupported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED"></span><span id="e_imapi_erase_recorder_not_supported"></span><dl> <span data-ttu-id="bd977-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aa090a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-301"><dt><strong>E_IMAPI_ERASE_RECORDER_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AA090A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-302">Dieses Gerät unterstützt nicht die Vorgänge, die für dieses Festplatten Format erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bd977-302">This device does not support the operations required by this disc format.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID"></span><span id="e_imapi_erase_client_name_is_not_valid"></span><dl> <span data-ttu-id="bd977-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT) 0xc0aa090b</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-303"><dt><strong>E_IMAPI_ERASE_CLIENT_NAME_IS_NOT_VALID</strong></dt> <dt>(HRESULT)0xC0AA090B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-304">Der Client Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-304">The client name is not valid.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="bd977-305">Die folgenden Erfolgs-und Fehlercodes sind in Imapi2fserror. h definiert.</span><span class="sxs-lookup"><span data-stu-id="bd977-305">The following success and error codes are defined in Imapi2fserror.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="bd977-306">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="bd977-306">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="bd977-307">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd977-307">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FSI_INTERNAL_ERROR"></span><span id="imapi_e_fsi_internal_error"></span><dl> <span data-ttu-id="bd977-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT) 0xc0aab100</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-308"><dt><strong>IMAPI_E_FSI_INTERNAL_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-309">Interner Fehler: %1! ls!.</span><span class="sxs-lookup"><span data-stu-id="bd977-309">Internal error occurred: %1!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PARAM"></span><span id="imapi_e_invalid_param"></span><dl> <span data-ttu-id="bd977-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT) 0xc0aab101</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-310"><dt><strong>IMAPI_E_INVALID_PARAM</strong></dt> <dt>(HRESULT)0xC0AAB101</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-311">Der für den Parameter "%1! ls!" angegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="bd977-311">The value specified for parameter '%1!ls!'</span></span> <span data-ttu-id="bd977-312">ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-312">is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_READONLY"></span><span id="imapi_e_readonly"></span><dl> <span data-ttu-id="bd977-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT) 0xc0aab102</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-313"><dt><strong>IMAPI_E_READONLY</strong></dt> <dt>(HRESULT)0xC0AAB102</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-314">Das filesystemimage-Objekt befindet sich im schreibgeschützten Modus.</span><span class="sxs-lookup"><span data-stu-id="bd977-314">FileSystemImage object is in read only mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_OUTPUT"></span><span id="imapi_e_no_output"></span><dl> <span data-ttu-id="bd977-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT) 0xc0aab103</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-315"><dt><strong>IMAPI_E_NO_OUTPUT</strong></dt> <dt>(HRESULT)0xC0AAB103</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-316">Es wurde kein Ausgabedatei System angegeben.</span><span class="sxs-lookup"><span data-stu-id="bd977-316">No output file system specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_VOLUME_NAME"></span><span id="imapi_e_invalid_volume_name"></span><dl> <span data-ttu-id="bd977-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT) 0xc0aab104</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-317"><dt><strong>IMAPI_E_INVALID_VOLUME_NAME</strong></dt> <dt>(HRESULT)0xC0AAB104</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-318">Die angegebene Volumekennung ist entweder zu lang oder enthält mindestens ein ungültiges Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bd977-318">The specified Volume Identifier is either too long or contains one or more invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_DATE"></span><span id="imapi_e_invalid_date"></span><dl> <span data-ttu-id="bd977-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT) 0xc0aab105</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-319"><dt><strong>IMAPI_E_INVALID_DATE</strong></dt> <dt>(HRESULT)0xC0AAB105</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-320">Ungültige Datumsangaben.</span><span class="sxs-lookup"><span data-stu-id="bd977-320">Invalid file dates.</span></span> <span data-ttu-id="bd977-321">%1! ls!</span><span class="sxs-lookup"><span data-stu-id="bd977-321">%1!ls!</span></span> <span data-ttu-id="bd977-322">die Uhrzeit liegt vor %2! ls!</span><span class="sxs-lookup"><span data-stu-id="bd977-322">time is earlier than %2!ls!</span></span> <span data-ttu-id="bd977-323">kann.</span><span class="sxs-lookup"><span data-stu-id="bd977-323">time.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_EMPTY"></span><span id="imapi_e_file_system_not_empty"></span><dl> <span data-ttu-id="bd977-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xc0aab106</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-324"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB106</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-325">Das Dateisystem muss für diese Funktion leer sein.</span><span class="sxs-lookup"><span data-stu-id="bd977-325">The file system must be empty for this function.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED"></span><span id="imapi_e_file_system_change_not_allowed"></span><dl> <span data-ttu-id="bd977-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xc0aab163l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-326"><dt><strong>IMAPI_E_FILE_SYSTEM_CHANGE_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB163L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-327">Sie können das für die Erstellung angegebene Dateisystem nicht ändern, da das Dateisystem aus der importierten Sitzung und das Dateisystem in der aktuellen Sitzung nicht mit identisch sind.</span><span class="sxs-lookup"><span data-stu-id="bd977-327">You cannot change the file system specified for creation, because the file system from the imported session and the file system in the current session do not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_NOT_FILE"></span><span id="imapi_e_not_file"></span><dl> <span data-ttu-id="bd977-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT) 0xc0aab108</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-328"><dt><strong>IMAPI_E_NOT_FILE</strong></dt> <dt>(HRESULT)0xC0AAB108</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-329">Der angegebene Pfad "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="bd977-329">Specified path '%1!ls!'</span></span> <span data-ttu-id="bd977-330">identifiziert keine Datei.</span><span class="sxs-lookup"><span data-stu-id="bd977-330">does not identify a file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_DIR"></span><span id="imapi_e_not_dir"></span><dl> <span data-ttu-id="bd977-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT) 0xc0aab109</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-331"><dt><strong>IMAPI_E_NOT_DIR</strong></dt> <dt>(HRESULT)0xC0AAB109</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-332">Der angegebene Pfad "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="bd977-332">Specified path '%1!ls!'</span></span> <span data-ttu-id="bd977-333">identifiziert kein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="bd977-333">does not identify a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_EMPTY"></span><span id="imapi_e_dir_not_empty"></span><dl> <span data-ttu-id="bd977-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT) 0xc0aab10a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-334"><dt><strong>IMAPI_E_DIR_NOT_EMPTY</strong></dt> <dt>(HRESULT)0xC0AAB10A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-335">Das Verzeichnis "%1! s!".</span><span class="sxs-lookup"><span data-stu-id="bd977-335">The directory '%1!s!'</span></span> <span data-ttu-id="bd977-336">ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="bd977-336">is not empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NOT_IN_FILE_SYSTEM"></span><span id="imapi_e_not_in_file_system"></span><dl> <span data-ttu-id="bd977-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xc0aab10b</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-337"><dt><strong>IMAPI_E_NOT_IN_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB10B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-338">ls! "</span><span class="sxs-lookup"><span data-stu-id="bd977-338">ls!'</span></span> <span data-ttu-id="bd977-339">ist nicht Teil des Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="bd977-339">is not part of the file system.</span></span> <span data-ttu-id="bd977-340">Sie muss hinzugefügt werden, um diesen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bd977-340">It must be added to complete this operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_PATH"></span><span id="imapi_e_invalid_path"></span><dl> <span data-ttu-id="bd977-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT) 0xc0aab110</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-341"><dt><strong>IMAPI_E_INVALID_PATH</strong></dt> <dt>(HRESULT)0xC0AAB110</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-342">Pfad "%1! s!"</span><span class="sxs-lookup"><span data-stu-id="bd977-342">Path '%1!s!'</span></span> <span data-ttu-id="bd977-343">ist falsch formatiert oder enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bd977-343">is badly formed or contains invalid characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_RESTRICTED_NAME_VIOLATION"></span><span id="imapi_e_restricted_name_violation"></span><dl> <span data-ttu-id="bd977-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT) 0xc0aab111</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-344"><dt><strong>IMAPI_E_RESTRICTED_NAME_VIOLATION</strong></dt> <dt>(HRESULT)0xC0AAB111</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-345">Der Name "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="bd977-345">The name '%1!ls!'</span></span> <span data-ttu-id="bd977-346">angegeben ist nicht zulässig: der Name der Datei oder des Verzeichnis Objekts, das erstellt wird, während die userestrictedcharakteriset-Eigenschaft festgelegt ist, darf nur ANSI-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd977-346">specified is not legal: Name of file or directory object created while the UseRestrictedCharacterSet property is set may only contain ANSI characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DUP_NAME"></span><span id="imapi_e_dup_name"></span><dl> <span data-ttu-id="bd977-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT) 0xc0aab112</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-347"><dt><strong>IMAPI_E_DUP_NAME</strong></dt> <dt>(HRESULT)0xC0AAB112</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-348">ls! "</span><span class="sxs-lookup"><span data-stu-id="bd977-348">ls!'</span></span> <span data-ttu-id="bd977-349">der Name ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bd977-349">name already exists.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_UNIQUE_NAME"></span><span id="imapi_e_no_unique_name"></span><dl> <span data-ttu-id="bd977-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT) 0xc0aab113</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-350"><dt><strong>IMAPI_E_NO_UNIQUE_NAME</strong></dt> <dt>(HRESULT)0xC0AAB113</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-351">Es wurde versucht, "%1! ls!" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bd977-351">Attempt to add '%1!ls!'</span></span> <span data-ttu-id="bd977-352">Fehler: Es kann kein Dateisystem spezifischer eindeutiger Name für "%2! ls!" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-352">failed: cannot create a file-system-specific unique name for the %2!ls!</span></span> <span data-ttu-id="bd977-353">-Dateisystem durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-353">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ITEM_NOT_FOUND"></span><span id="imapi_e_item_not_found"></span><dl> <span data-ttu-id="bd977-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab118</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-354"><dt><strong>IMAPI_E_ITEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB118</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-355">Das Element "%1! ls!" wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="bd977-355">Cannot find item '%1!ls!'</span></span> <span data-ttu-id="bd977-356">in der filesystemimage-Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="bd977-356">in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_NOT_FOUND"></span><span id="imapi_e_file_not_found"></span><dl> <span data-ttu-id="bd977-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab119</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-357"><dt><strong>IMAPI_E_FILE_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB119</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-358">Die Datei ' %1! s! '</span><span class="sxs-lookup"><span data-stu-id="bd977-358">The file '%1!s!'</span></span> <span data-ttu-id="bd977-359">in der filesystemimage-Hierarchie nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="bd977-359">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIR_NOT_FOUND"></span><span id="imapi_e_dir_not_found"></span><dl> <span data-ttu-id="bd977-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab11a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-360"><dt><strong>IMAPI_E_DIR_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB11A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-361">Das Verzeichnis "%1! s!".</span><span class="sxs-lookup"><span data-stu-id="bd977-361">The directory '%1!s!'</span></span> <span data-ttu-id="bd977-362">in der filesystemimage-Hierarchie nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="bd977-362">not found in FileSystemImage hierarchy.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_SIZE_LIMIT"></span><span id="imapi_e_image_size_limit"></span><dl> <span data-ttu-id="bd977-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT) 0xc0aab120</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-363"><dt><strong>IMAPI_E_IMAGE_SIZE_LIMIT</strong></dt> <dt>(HRESULT)0xC0AAB120</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-364">"%1! ls!" wird hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bd977-364">Adding '%1!ls!'</span></span> <span data-ttu-id="bd977-365">würde dazu führen, dass ein Ergebnisbild größer als das aktuell konfigurierte Limit ist.</span><span class="sxs-lookup"><span data-stu-id="bd977-365">would result in a result image having a size larger than the current configured limit.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGE_TOO_BIG"></span><span id="imapi_e_image_too_big"></span><dl> <span data-ttu-id="bd977-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xc0aab121</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-366"><dt><strong>IMAPI_E_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB121</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-367">Der für die Eigenschaft "fremediablocks" angegebene Wert ist zu klein für die geschätzte Bild Größe basierend auf den aktuellen Daten.</span><span class="sxs-lookup"><span data-stu-id="bd977-367">Value specified for FreeMediaBlocks property is too small for estimated image size based on current data.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED"></span><span id="imapi_e_imagemanager_image_not_aligned"></span><dl> <span data-ttu-id="bd977-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT) 0xc0aab200l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-368"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_NOT_ALIGNED</strong></dt> <dt>(HRESULT)0xC0AAB200L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-369">Das Bild wird nicht an einer Sektorgrenze von 2 KB ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="bd977-369">The image is not aligned on a 2kb sector boundary.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND"></span><span id="imapi_e_imagemanager_no_valid_vd_found"></span><dl> <span data-ttu-id="bd977-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab201l)</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-370"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_VALID_VD_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB201L)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-371">Das Image enthält keinen gültigen volumedeskriptor.</span><span class="sxs-lookup"><span data-stu-id="bd977-371">The image does not contain a valid volume descriptor.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_NO_IMAGE"></span><span id="imapi_e_imagemanager_no_image"></span><dl> <span data-ttu-id="bd977-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT) 0xc0aab202l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-372"><dt><strong>IMAPI_E_IMAGEMANAGER_NO_IMAGE</strong></dt> <dt>(HRESULT)0xC0AAB202L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-373">Das Image wurde nicht mithilfe der <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>iisoimagemanager:: setpath</strong></a> -Methode oder der <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>iisoimagemanager:: setStream</strong></a> -Methode festgelegt, bevor die <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>iisoimagemanager:: Validate</strong></a> -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="bd977-373">The image has not been set using the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setpath"><strong>IIsoImageManager::SetPath</strong></a> or <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-setstream"><strong>IIsoImageManager::SetStream</strong></a> methods prior to calling the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iisoimagemanager-validate"><strong>IIsoImageManager::Validate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG"></span><span id="imapi_e_imagemanager_image_too_big"></span><dl> <span data-ttu-id="bd977-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT) 0xc0aab203l</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-374"><dt><strong>IMAPI_E_IMAGEMANAGER_IMAGE_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB203L</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-375">Das angegebene Bild ist zu groß, um überprüft werden zu können, wenn die Größe <strong>MAXLONG</strong>überschreitet.</span><span class="sxs-lookup"><span data-stu-id="bd977-375">The provided image is too large to be validated as the size exceeds <strong>MAXLONG</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_INCONSISTENCY"></span><span id="imapi_e_data_stream_inconsistency"></span><dl> <span data-ttu-id="bd977-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT) 0xc0aab128</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-376"><dt><strong>IMAPI_E_DATA_STREAM_INCONSISTENCY</strong></dt> <dt>(HRESULT)0xC0AAB128</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-377">Der für die Datei "%1! ls!" angegebene Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="bd977-377">Data stream supplied for file '%1!ls!'</span></span> <span data-ttu-id="bd977-378">inkonsistent: erwartet: %2! I64d!</span><span class="sxs-lookup"><span data-stu-id="bd977-378">is inconsistent: expected %2!I64d!</span></span> <span data-ttu-id="bd977-379">bytes, gefunden: %3! I64d!.</span><span class="sxs-lookup"><span data-stu-id="bd977-379">bytes, found %3!I64d!.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_READ_FAILURE"></span><span id="imapi_e_data_stream_read_failure"></span><dl> <span data-ttu-id="bd977-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab129</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-380"><dt><strong>IMAPI_E_DATA_STREAM_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB129</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-381">Es können keine Daten aus dem Stream für die Datei "%1! ls!" gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-381">Cannot read data from stream supplied for file '%1!ls!'.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_STREAM_CREATE_FAILURE"></span><span id="imapi_e_data_stream_create_failure"></span><dl> <span data-ttu-id="bd977-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab12a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-382"><dt><strong>IMAPI_E_DATA_STREAM_CREATE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-383">Fehler beim Erstellen des Datenstroms für die Datei "%1! ls!":</span><span class="sxs-lookup"><span data-stu-id="bd977-383">The following error was encountered when trying to create data stream for file '%1!ls!':</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DIRECTORY_READ_FAILURE"></span><span id="imapi_e_directory_read_failure"></span><dl> <span data-ttu-id="bd977-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab12bl</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-384"><dt><strong>IMAPI_E_DIRECTORY_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB12BL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-385">Fehler beim Aufzählen von Dateien in der Verzeichnisstruktur aufgrund von Berechtigungen nicht.</span><span class="sxs-lookup"><span data-stu-id="bd977-385">Failure enumerating files in the directory tree is inaccessible due to permissions.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_TOO_MANY_DIRS"></span><span id="imapi_e_too_many_dirs"></span><dl> <span data-ttu-id="bd977-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT) 0xc0aab130</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-386"><dt><strong>IMAPI_E_TOO_MANY_DIRS</strong></dt> <dt>(HRESULT)0xC0AAB130</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-387">Dieses Dateisystem Image enthält zu viele Verzeichnisse für "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="bd977-387">This file system image has too many directories for the %1!ls!</span></span> <span data-ttu-id="bd977-388">-Dateisystem durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-388">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_ISO9660_LEVELS"></span><span id="imapi_e_iso9660_levels"></span><dl> <span data-ttu-id="bd977-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT) 0xc0aab131</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-389"><dt><strong>IMAPI_E_ISO9660_LEVELS</strong></dt> <dt>(HRESULT)0xC0AAB131</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-390">ISO9660 ist auf 8 Ebenen von Verzeichnissen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="bd977-390">ISO9660 is limited to 8 levels of directories.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_DATA_TOO_BIG"></span><span id="imapi_e_data_too_big"></span><dl> <span data-ttu-id="bd977-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT) 0xc0aab132</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-391"><dt><strong>IMAPI_E_DATA_TOO_BIG</strong></dt> <dt>(HRESULT)0xC0AAB132</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-392">Die Datendatei ist zu groß für "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="bd977-392">Data file is too large for '%1!ls!'</span></span> <span data-ttu-id="bd977-393">-Dateisystem durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-393">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_OPEN_FAILURE"></span><span id="imapi_e_stashfile_open_failure"></span><dl> <span data-ttu-id="bd977-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab138</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-394"><dt><strong>IMAPI_E_STASHFILE_OPEN_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB138</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-395">%1! ls! kann nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-395">Cannot initialize %1!ls!</span></span> <span data-ttu-id="bd977-396">Stash-Datei.</span><span class="sxs-lookup"><span data-stu-id="bd977-396">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_SEEK_FAILURE"></span><span id="imapi_e_stashfile_seek_failure"></span><dl> <span data-ttu-id="bd977-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab139</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-397"><dt><strong>IMAPI_E_STASHFILE_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB139</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-398">Fehler beim Suchen in "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="bd977-398">Error seeking in '%1!ls!'</span></span> <span data-ttu-id="bd977-399">Stash-Datei.</span><span class="sxs-lookup"><span data-stu-id="bd977-399">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_WRITE_FAILURE"></span><span id="imapi_e_stashfile_write_failure"></span><dl> <span data-ttu-id="bd977-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab13a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-400"><dt><strong>IMAPI_E_STASHFILE_WRITE_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-401">Fehler beim Schreiben in "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="bd977-401">Error encountered writing to '%1!ls!'</span></span> <span data-ttu-id="bd977-402">Stash-Datei.</span><span class="sxs-lookup"><span data-stu-id="bd977-402">stash file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_READ_FAILURE"></span><span id="imapi_e_stashfile_read_failure"></span><dl> <span data-ttu-id="bd977-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab13b</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-403"><dt><strong>IMAPI_E_STASHFILE_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB13B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-404">Fehler beim Lesen von "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="bd977-404">Error encountered reading from '%1!ls!'</span></span> <span data-ttu-id="bd977-405">Stash-Datei.</span><span class="sxs-lookup"><span data-stu-id="bd977-405">stash file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INVALID_WORKING_DIRECTORY"></span><span id="imapi_e_invalid_working_directory"></span><dl> <span data-ttu-id="bd977-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT) 0xc0aab140</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-406"><dt><strong>IMAPI_E_INVALID_WORKING_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB140</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-407">Das Arbeitsverzeichnis "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="bd977-407">The working directory '%1!ls!'</span></span> <span data-ttu-id="bd977-408">ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bd977-408">is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_WORKING_DIRECTORY_SPACE"></span><span id="imapi_e_working_directory_space"></span><dl> <span data-ttu-id="bd977-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT) 0xc0aab141</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-409"><dt><strong>IMAPI_E_WORKING_DIRECTORY_SPACE</strong></dt> <dt>(HRESULT)0xC0AAB141</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-410">Das Arbeitsverzeichnis kann nicht auf "%1! ls!" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-410">Cannot set working directory to '%1!ls!'.</span></span> <span data-ttu-id="bd977-411">Verfügbarer Speicherplatz: %2! I64d!</span><span class="sxs-lookup"><span data-stu-id="bd977-411">Space available is %2!I64d!</span></span> <span data-ttu-id="bd977-412">bytes, ungefähr %3! I64d!</span><span class="sxs-lookup"><span data-stu-id="bd977-412">bytes, approximately %3!I64d!</span></span> <span data-ttu-id="bd977-413">erforderliche bytes.</span><span class="sxs-lookup"><span data-stu-id="bd977-413">bytes required.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_STASHFILE_MOVE"></span><span id="imapi_e_stashfile_move"></span><dl> <span data-ttu-id="bd977-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT) 0xc0aab142</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-414"><dt><strong>IMAPI_E_STASHFILE_MOVE</strong></dt> <dt>(HRESULT)0xC0AAB142</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-415">Es wurde versucht, die Datenstapel Datei in das Verzeichnis "%1! ls!" zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="bd977-415">Attempt to move the data stash file to directory '%1!ls!'</span></span> <span data-ttu-id="bd977-416">konnte nicht erfolgreich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-416">was not successful.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_IMAGE_DATA"></span><span id="imapi_e_boot_image_data"></span><dl> <span data-ttu-id="bd977-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT) 0xc0aab148</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-417"><dt><strong>IMAPI_E_BOOT_IMAGE_DATA</strong></dt> <dt>(HRESULT)0xC0AAB148</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-418">Das Start Objekt konnte dem Bild nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-418">The boot object could not be added to the image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_OBJECT_CONFLICT"></span><span id="imapi_e_boot_object_conflict"></span><dl> <span data-ttu-id="bd977-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT) 0xc0aab149</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-419"><dt><strong>IMAPI_E_BOOT_OBJECT_CONFLICT</strong></dt> <dt>(HRESULT)0xC0AAB149</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-420">Ein Start Objekt kann nur in einem ersten Festplatten Abbild enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="bd977-420">A boot object can only be included in an initial disc image.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH"></span><span id="imapi_e_boot_emulation_image_size_mismatch"></span><dl> <span data-ttu-id="bd977-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT) 0xc0aab14a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-421"><dt><strong>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB14A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-422">Der angeforderte Emulationstyp entspricht nicht der Größe des Start Abbilds.</span><span class="sxs-lookup"><span data-stu-id="bd977-422">The emulation type requested does not match the boot image size.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_EMPTY_DISC"></span><span id="imapi_e_empty_disc"></span><dl> <span data-ttu-id="bd977-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT) 0xc0aab150</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-423"><dt><strong>IMAPI_E_EMPTY_DISC</strong></dt> <dt>(HRESULT)0xC0AAB150</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-424">Optische Medien sind leer.</span><span class="sxs-lookup"><span data-stu-id="bd977-424">Optical media is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_SUPPORTED_FILE_SYSTEM"></span><span id="imapi_e_no_supported_file_system"></span><dl> <span data-ttu-id="bd977-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT) 0xc0aab151</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-425"><dt><strong>IMAPI_E_NO_SUPPORTED_FILE_SYSTEM</strong></dt> <dt>(HRESULT)0xC0AAB151</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-426">Die angegebene Festplatte enthält keines der unterstützten Dateisysteme.</span><span class="sxs-lookup"><span data-stu-id="bd977-426">The specified disc does not contain one of the supported file systems.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_NOT_FOUND"></span><span id="imapi_e_file_system_not_found"></span><dl> <span data-ttu-id="bd977-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT) 0xc0aab152</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-427"><dt><strong>IMAPI_E_FILE_SYSTEM_NOT_FOUND</strong></dt> <dt>(HRESULT)0xC0AAB152</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-428">Die angegebene Festplatte enthält kein "%1! ls!".</span><span class="sxs-lookup"><span data-stu-id="bd977-428">The specified disc does not contain a '%1!ls!'</span></span> <span data-ttu-id="bd977-429">-Dateisystem durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-429">file system.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR"></span><span id="imapi_e_file_system_read_consistency_error"></span><dl> <span data-ttu-id="bd977-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT) 0xc0aab153</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-430"><dt><strong>IMAPI_E_FILE_SYSTEM_READ_CONSISTENCY_ERROR</strong></dt> <dt>(HRESULT)0xC0AAB153</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-431">Beim Importieren von "%1! ls!" ist ein Konsistenz Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="bd977-431">Consistency error encountered while importing the '%1!ls!'</span></span> <span data-ttu-id="bd977-432">-Dateisystem durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd977-432">file system.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED"></span><span id="imapi_e_file_system_feature_not_supported"></span><dl> <span data-ttu-id="bd977-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0xc0aab154</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-433"><dt><strong>IMAPI_E_FILE_SYSTEM_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0xC0AAB154</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-434">"%1! ls!" das Dateisystem auf der ausgewählten CD enthält ein Feature, das für den Import nicht unterstützt wird: %2! ls!.</span><span class="sxs-lookup"><span data-stu-id="bd977-434">The '%1!ls!'file system on the selected disc contains a feature not supported for import: %2!ls!.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY"></span><span id="imapi_e_import_type_collision_file_exists_as_directory"></span><dl> <span data-ttu-id="bd977-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT) 0xc0aab155</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-435"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_FILE_EXISTS_AS_DIRECTORY</strong></dt> <dt>(HRESULT)0xC0AAB155</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-436">"%2! ls!" konnte nicht importiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-436">Could not import %2!ls!</span></span> <span data-ttu-id="bd977-437">Dateisystem von Disk. Die Datei "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="bd977-437">file system from disc. The file '%1!ls!'</span></span> <span data-ttu-id="bd977-438">ist bereits in der Bild Hierarchie als Verzeichnis vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bd977-438">already exists within the image hierarchy as a directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_SEEK_FAILURE"></span><span id="imapi_e_import_seek_failure"></span><dl> <span data-ttu-id="bd977-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab156</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-439"><dt><strong>IMAPI_E_IMPORT_SEEK_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB156</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-440">"%1" kann nicht durchsucht werden. I64d!</span><span class="sxs-lookup"><span data-stu-id="bd977-440">Cannot seek to block %1!I64d!</span></span> <span data-ttu-id="bd977-441">auf der Quell-CD.</span><span class="sxs-lookup"><span data-stu-id="bd977-441">on source disc.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_READ_FAILURE"></span><span id="imapi_e_import_read_failure"></span><dl> <span data-ttu-id="bd977-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT) 0xc0aab157</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-442"><dt><strong>IMAPI_E_IMPORT_READ_FAILURE</strong></dt> <dt>(HRESULT)0xC0AAB157</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-443">Fehler beim Importieren aus vorheriger Sitzung aufgrund eines Fehlers beim Lesen eines Blocks auf dem Medium (wahrscheinlichste Block: %1! u!).</span><span class="sxs-lookup"><span data-stu-id="bd977-443">Import from previous session failed due to an error reading a block on the media (most likely block %1!u!).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_DISC_MISMATCH"></span><span id="imapi_e_disc_mismatch"></span><dl> <span data-ttu-id="bd977-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT) 0xc0aab158</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-444"><dt><strong>IMAPI_E_DISC_MISMATCH</strong></dt> <dt>(HRESULT)0xC0AAB158</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-445">Der aktuelle Datenträger ist nicht der gleiche, von dem das Dateisystem importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bd977-445">Current disc is not the same one from which file system was imported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED"></span><span id="imapi_e_import_media_not_allowed"></span><dl> <span data-ttu-id="bd977-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT) 0xc0aab159</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-446"><dt><strong>IMAPI_E_IMPORT_MEDIA_NOT_ALLOWED</strong></dt> <dt>(HRESULT)0xC0AAB159</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-447">IMAPI lässt keine mehrfach Sitzung mit dem aktuellen Medientyp zu.</span><span class="sxs-lookup"><span data-stu-id="bd977-447">IMAPI does not allow multi-session with the current media type.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_UDF_NOT_WRITE_COMPATIBLE"></span><span id="imapi_e_udf_not_write_compatible"></span><dl> <span data-ttu-id="bd977-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT) 0xc0aab15a</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-448"><dt><strong>IMAPI_E_UDF_NOT_WRITE_COMPATIBLE</strong></dt> <dt>(HRESULT)0xC0AAB15A</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-449">IMAPI kann nicht mehrere Sitzungen mit dem aktuellen Medium ausführen, da keine kompatible UDF-Revision zum Schreiben unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="bd977-449">IMAPI cannot do multi-session with the current media because it does not support a compatible UDF revision for write.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_incompatible_multisession_type"></span><dl> <span data-ttu-id="bd977-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xc0aab15b</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-450"><dt><strong>IMAPI_E_INCOMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15B</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-451">IMAPI unterstützt den angeforderten multisitzungstyp nicht.</span><span class="sxs-lookup"><span data-stu-id="bd977-451">IMAPI does not support the multisession type requested.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION"></span><span id="imapi_e_incompatible_previous_session"></span><dl> <span data-ttu-id="bd977-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT) 0xc0aab133</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-452"><dt><strong>IMAPI_E_INCOMPATIBLE_PREVIOUS_SESSION</strong></dt> <dt>(HRESULT)0xC0AAB133</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-453">Fehler beim Vorgang aufgrund eines nicht kompatiblen Layouts der vorherigen Sitzung, die aus dem Medium importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bd977-453">Operation failed due to an incompatible layout of the previous session imported from the medium.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE"></span><span id="imapi_e_no_compatible_multisession_type"></span><dl> <span data-ttu-id="bd977-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT) 0xc0aab15c</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-454"><dt><strong>IMAPI_E_NO_COMPATIBLE_MULTISESSION_TYPE</strong></dt> <dt>(HRESULT)0xC0AAB15C</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-455">IMAPI unterstützt keine der multisitzungstyp (e), die auf dem aktuellen Medium bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-455">IMAPI supports none of the multisession type(s) provided on the current media.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bd977-456">[<strong>Ifilesystemimage:: ImportFile System</strong>] (/Windows/Desktop/API/IMAPI2FS/NF-IMAPI2FS-ifilesystemimage-importfilesystem)-Methode gibt diesen Fehler zurück, wenn das Aufzeichnungsgerät keine Medien enthält.</span><span class="sxs-lookup"><span data-stu-id="bd977-456">[<strong>IFileSystemImage::ImportFileSystem</strong>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method returns this error if there is no media in the recording device.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_MULTISESSION_NOT_SET"></span><span id="imapi_e_multisession_not_set"></span><dl> <span data-ttu-id="bd977-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT) 0xc0aab15d</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-457"><dt><strong>IMAPI_E_MULTISESSION_NOT_SET</strong></dt> <dt>(HRESULT)0xC0AAB15D</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-458">Die multisessioninterfaces-Eigenschaft muss festgelegt werden, bevor diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bd977-458">MultisessionInterfaces property must be set prior calling this method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE"></span><span id="imapi_e_import_type_collision_directory_exists_as_file"></span><dl> <span data-ttu-id="bd977-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT) 0xc0aab15e</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-459"><dt><strong>IMAPI_E_IMPORT_TYPE_COLLISION_DIRECTORY_EXISTS_AS_FILE</strong></dt> <dt>(HRESULT)0xC0AAB15E</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-460">"%2! ls!" konnte nicht importiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd977-460">Could not import %2!ls!</span></span> <span data-ttu-id="bd977-461">Dateisystem von Disk. Das Verzeichnis "%1! ls!"</span><span class="sxs-lookup"><span data-stu-id="bd977-461">file system from disc. The directory '%1!ls!'</span></span> <span data-ttu-id="bd977-462">ist in der Bild Hierarchie bereits als Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bd977-462">already exists within the image hierarchy as a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="IMAPI_E_BAD_MULTISESSION_PARAMETER"></span><span id="imapi_e_bad_multisession_parameter"></span><dl> <span data-ttu-id="bd977-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT) 0xc0aab162</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-463"><dt><strong>IMAPI_E_BAD_MULTISESSION_PARAMETER</strong></dt> <dt>(HRESULT)0xC0AAB162</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-464">Einer der Parameter für mehrere Sitzungen kann nicht abgerufen werden oder weist einen falschen Wert auf.</span><span class="sxs-lookup"><span data-stu-id="bd977-464">One of multisession parameters cannot be retrieved or has a wrong value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED"></span><span id="imapi_s_image_feature_not_supported"></span><dl> <span data-ttu-id="bd977-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT) 0x00aab15fl</dt> </span><span class="sxs-lookup"><span data-stu-id="bd977-465"><dt><strong>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</strong></dt> <dt>(HRESULT)0x00AAB15FL</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bd977-466">Diese Funktion wird für die aktuelle Dateisystem Revision nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd977-466">This feature is not supported for the current file system revision.</span></span> <span data-ttu-id="bd977-467">Das Image wird ohne diese Funktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="bd977-467">The image will be created without this feature.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="bd977-468">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd977-468">Requirements</span></span>



| <span data-ttu-id="bd977-469">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd977-469">Requirement</span></span> | <span data-ttu-id="bd977-470">Wert</span><span class="sxs-lookup"><span data-stu-id="bd977-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd977-471">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd977-471">Minimum supported client</span></span><br/> | <span data-ttu-id="bd977-472">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd977-472">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="bd977-473">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd977-473">Minimum supported server</span></span><br/> | <span data-ttu-id="bd977-474">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd977-474">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                            |
| <span data-ttu-id="bd977-475">Header</span><span class="sxs-lookup"><span data-stu-id="bd977-475">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd977-476"><dt>Imapi2error. h; </dt> <dt>Imapi2fserror. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd977-476"><dt>Imapi2error.h; </dt> <dt>Imapi2fserror.h</dt></span></span> </dl> |



 

 





