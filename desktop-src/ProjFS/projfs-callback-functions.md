---
title: Projfs-Rückruf Funktionen
description: Die folgenden Rückruf Funktionen werden in projectedfslib. h deklariert.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2020
ms.locfileid: "103857940"
---
# <a name="callback-functions"></a><span data-ttu-id="53a8b-103">Rückruf Funktionen</span><span class="sxs-lookup"><span data-stu-id="53a8b-103">Callback functions</span></span>

<span data-ttu-id="53a8b-104">Die folgenden Rückruf Funktionen werden in projectedfslib. h deklariert.</span><span class="sxs-lookup"><span data-stu-id="53a8b-104">The following callback functions are declared in projectedfslib.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="53a8b-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="53a8b-105">In this section</span></span>

| <span data-ttu-id="53a8b-106">Thema</span><span class="sxs-lookup"><span data-stu-id="53a8b-106">Topic</span></span> | <span data-ttu-id="53a8b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53a8b-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="53a8b-108">**PRJ_CANCEL_COMMAND_CB**</span><span class="sxs-lookup"><span data-stu-id="53a8b-108">**PRJ_CANCEL_COMMAND_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | <span data-ttu-id="53a8b-109">Benachrichtigt den Anbieter, dass ein Vorgang eines früheren Aufrufs eines Rückrufs abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="53a8b-109">Notifies the provider that an operation by an earlier invocation of a callback should be canceled.</span></span> |
| [<span data-ttu-id="53a8b-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="53a8b-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | <span data-ttu-id="53a8b-111">Informiert den Anbieter darüber, dass sich eine verzeichnisenumeration befindet.</span><span class="sxs-lookup"><span data-stu-id="53a8b-111">Informs the provider that a directory enumeration is over.</span></span> |
| [<span data-ttu-id="53a8b-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="53a8b-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | <span data-ttu-id="53a8b-113">Fordert verzeichnisenumerationsinformationen vom Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="53a8b-113">Requests directory enumeration information from the provider.</span></span>
| [<span data-ttu-id="53a8b-114">**PRJ_GET_FILE_DATA_CB**</span><span class="sxs-lookup"><span data-stu-id="53a8b-114">**PRJ_GET_FILE_DATA_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | <span data-ttu-id="53a8b-115">Fordert den Inhalt des primären Datenstroms einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="53a8b-115">Requests the contents of a file's primary data stream.</span></span>
| [<span data-ttu-id="53a8b-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span><span class="sxs-lookup"><span data-stu-id="53a8b-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | <span data-ttu-id="53a8b-117">Fordert Informationen für eine Datei oder ein Verzeichnis vom Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="53a8b-117">Requests information for a file or directory from the provider.</span></span>
| [<span data-ttu-id="53a8b-118">**PRJ_NOTIFICATION_CB**</span><span class="sxs-lookup"><span data-stu-id="53a8b-118">**PRJ_NOTIFICATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | <span data-ttu-id="53a8b-119">Übermittelt Benachrichtigungen an den Anbieter zu Dateisystem Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="53a8b-119">Delivers notifications to the provider about file system operations.</span></span>
| [<span data-ttu-id="53a8b-120">**PRJ_QUERY_FILE_NAME_CB**</span><span class="sxs-lookup"><span data-stu-id="53a8b-120">**PRJ_QUERY_FILE_NAME_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | <span data-ttu-id="53a8b-121">Bestimmt, ob ein angegebener Dateipfad im Sicherungs Speicher des Anbieters vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="53a8b-121">Determines whether a given file path exists in the provider's backing store.</span></span>
| [<span data-ttu-id="53a8b-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="53a8b-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | <span data-ttu-id="53a8b-123">Informiert den Anbieter darüber, dass eine verzeichnisenumeration gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="53a8b-123">Informs the provider that a directory enumeration is starting.</span></span>