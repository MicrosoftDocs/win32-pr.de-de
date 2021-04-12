---
description: Wenn eine Anwendung opportunistische Sperren anfordert, müssen alle Dateien, für die Sie Sperren anfordert, für überlappende (asynchrone) Eingaben und Ausgaben geöffnet werden, indem die Funktion "Funktion" mit dem überlappenden Flag für das Dateiflag verwendet wird \_ \_ .
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Opportunistische Sperr Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529138"
---
# <a name="opportunistic-lock-operations"></a><span data-ttu-id="aac26-103">Opportunistische Sperr Vorgänge</span><span class="sxs-lookup"><span data-stu-id="aac26-103">Opportunistic Lock Operations</span></span>

<span data-ttu-id="aac26-104">Wenn eine Anwendung opportunistische Sperren anfordert, müssen alle Dateien, für die Sie Sperren anfordert, für überlappende (asynchrone) Eingaben und Ausgaben geöffnet werden, indem [**die Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Funktion" mit dem überlappenden Flag für das **\_ Dateiflag \_** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aac26-104">If an application requests opportunistic locks, all files for which it requests locks must be opened for overlapped (asynchronous) input and output by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_OVERLAPPED** flag.</span></span> <span data-ttu-id="aac26-105">Nachdem die Dateien für einen überlappenden Vorgang geöffnet wurden, können Sie die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion mit einem der folgenden Kontrollcodes verwenden, um mit den opportunistischen Sperren dieser Dateien zu arbeiten:</span><span class="sxs-lookup"><span data-stu-id="aac26-105">After the files are opened for overlapped operation, you can use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with one of the following control codes to work with those files' opportunistic locks:</span></span>

<dl>

[<span data-ttu-id="aac26-106">**Schließen von "ssctl \_ opbatch \_ ACK" \_ steht \_ aus**</span><span class="sxs-lookup"><span data-stu-id="aac26-106">**FSCTL\_OPBATCH\_ACK\_CLOSE\_PENDING**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[<span data-ttu-id="aac26-107">**Ssctl- \_ Oplock- \_ break- \_ ACK Nr. \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="aac26-107">**FSCTL\_OPLOCK\_BREAK\_ACK\_NO\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[<span data-ttu-id="aac26-108">**losctl- \_ Oplock- \_ Abbruch \_ bestätigen**</span><span class="sxs-lookup"><span data-stu-id="aac26-108">**FSCTL\_OPLOCK\_BREAK\_ACKNOWLEDGE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[<span data-ttu-id="aac26-109">**Benachrichtigung zum Abbrechen der Sperre von "f" \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aac26-109">**FSCTL\_OPLOCK\_BREAK\_NOTIFY**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[<span data-ttu-id="aac26-110">**Sperre für den ssctl- \_ Anforderungs \_ Batch \_**</span><span class="sxs-lookup"><span data-stu-id="aac26-110">**FSCTL\_REQUEST\_BATCH\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[<span data-ttu-id="aac26-111">**\_Oplock für die Anforderung des volltextsfilters \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aac26-111">**FSCTL\_REQUEST\_FILTER\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[<span data-ttu-id="aac26-112">**Oplock für die ssctl- \_ Anforderung \_**</span><span class="sxs-lookup"><span data-stu-id="aac26-112">**FSCTL\_REQUEST\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[<span data-ttu-id="aac26-113">**Ssctl- \_ Anforderungs- \_ Oplock- \_ Ebene \_ 1**</span><span class="sxs-lookup"><span data-stu-id="aac26-113">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_1**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[<span data-ttu-id="aac26-114">**Ssctl- \_ Anforderungs- \_ Oplock- \_ Ebene \_ 2**</span><span class="sxs-lookup"><span data-stu-id="aac26-114">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
