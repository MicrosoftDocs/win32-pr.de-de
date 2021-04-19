---
description: Steuern Sie Codes und Strukturen, die mit dem Änderungs Journal für die NTFS-Dateisystem-Aktualisierungs Sequenznummer verwendet werden sollen.
ms.assetid: 2215f0d4-6ac8-42a5-87a5-9c76d1fae3ed
title: Ändern von Journal Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52cda51d0efc4cbae1333fc197f42d6a5cc0f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369022"
---
# <a name="change-journal-operations"></a><span data-ttu-id="c4621-103">Ändern von Journal Vorgängen</span><span class="sxs-lookup"><span data-stu-id="c4621-103">Change Journal Operations</span></span>

<span data-ttu-id="c4621-104">In der folgenden Liste sind die Steuerungs Codes aufgeführt, die mit dem Änderungs Journal des NTFS-Dateisystem-Aktualisierungs Sequenznummer (Aktualisierungs Sequenznummer) funktionieren.</span><span class="sxs-lookup"><span data-stu-id="c4621-104">The following list identifies the control codes that work with the NTFS file system update sequence number (USN) change journal.</span></span>

-   [<span data-ttu-id="c4621-105">**fisctl- \_ Create- \_ US- \_ Journal**</span><span class="sxs-lookup"><span data-stu-id="c4621-105">**FSCTL\_CREATE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [<span data-ttu-id="c4621-106">**f- \_ v-Lösch \_ \_ Journal**</span><span class="sxs-lookup"><span data-stu-id="c4621-106">**FSCTL\_DELETE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [<span data-ttu-id="c4621-107">**usctl \_ Enum- \_ \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="c4621-107">**FSCTL\_ENUM\_USN\_DATA**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [<span data-ttu-id="c4621-108">**\_Kennzeichen \_ handle**</span><span class="sxs-lookup"><span data-stu-id="c4621-108">**FSCTL\_MARK\_HANDLE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [<span data-ttu-id="c4621-109">**"f"- \_ Abfrage \_ \_ Journal**</span><span class="sxs-lookup"><span data-stu-id="c4621-109">**FSCTL\_QUERY\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [<span data-ttu-id="c4621-110">**Lese-und Schreib- \_ \_ \_ Journal von ssctl**</span><span class="sxs-lookup"><span data-stu-id="c4621-110">**FSCTL\_READ\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)

<span data-ttu-id="c4621-111">In der folgenden Liste sind die Strukturinformationen aufgeführt, die sich auf das Änderungs Journal für das NTFS-Dateisystem beziehen.</span><span class="sxs-lookup"><span data-stu-id="c4621-111">The following list identifies the structures information that relates to the NTFS file system USN change journal.</span></span>

-   [<span data-ttu-id="c4621-112">**Erstellen von \_ \_ Daten im \_ Daten Journal**</span><span class="sxs-lookup"><span data-stu-id="c4621-112">**CREATE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data)
-   [<span data-ttu-id="c4621-113">**Löschen von \_ \_ Daten im \_ Daten Journal**</span><span class="sxs-lookup"><span data-stu-id="c4621-113">**DELETE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-delete_usn_journal_data)
-   [<span data-ttu-id="c4621-114">**Info zum Markierungs \_ handle \_**</span><span class="sxs-lookup"><span data-stu-id="c4621-114">**MARK\_HANDLE\_INFO**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mark_handle_info)
-   [<span data-ttu-id="c4621-115">**MFT- \_ Enum- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="c4621-115">**MFT\_ENUM\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mft_enum_data_v0)
-   [<span data-ttu-id="c4621-116">**Lesen von \_ \_ Daten Journal \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="c4621-116">**READ\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)
-   [<span data-ttu-id="c4621-117">**Daten zum \_ Datenblatt des \_ Datenblatts**</span><span class="sxs-lookup"><span data-stu-id="c4621-117">**USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)
-   [<span data-ttu-id="c4621-118">**\_Datensatz**</span><span class="sxs-lookup"><span data-stu-id="c4621-118">**USN\_RECORD**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)

 

 
