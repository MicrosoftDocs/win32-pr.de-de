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
# <a name="opportunistic-lock-operations"></a>Opportunistische Sperr Vorgänge

Wenn eine Anwendung opportunistische Sperren anfordert, müssen alle Dateien, für die Sie Sperren anfordert, für überlappende (asynchrone) Eingaben und Ausgaben geöffnet werden, indem [**die Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Funktion" mit dem überlappenden Flag für das **\_ Dateiflag \_** verwendet wird. Nachdem die Dateien für einen überlappenden Vorgang geöffnet wurden, können Sie die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion mit einem der folgenden Kontrollcodes verwenden, um mit den opportunistischen Sperren dieser Dateien zu arbeiten:

<dl>

[**Schließen von "ssctl \_ opbatch \_ ACK" \_ steht \_ aus**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**Ssctl- \_ Oplock- \_ break- \_ ACK Nr. \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**losctl- \_ Oplock- \_ Abbruch \_ bestätigen**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**Benachrichtigung zum Abbrechen der Sperre von "f" \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**Sperre für den ssctl- \_ Anforderungs \_ Batch \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_Oplock für die Anforderung des volltextsfilters \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**Oplock für die ssctl- \_ Anforderung \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**Ssctl- \_ Anforderungs- \_ Oplock- \_ Ebene \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**Ssctl- \_ Anforderungs- \_ Oplock- \_ Ebene \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
