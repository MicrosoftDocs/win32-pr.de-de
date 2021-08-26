---
description: Wenn eine Anwendung deterministische Sperren an fordert, müssen alle Dateien, für die sie Sperren an fordert, für überlappende (asynchrone) Eingaben und Ausgaben geöffnet werden, indem die CreateFile-Funktion mit dem FLAG FILE FLAG OVERLAPPED verwendet \_ \_ wird.
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Deterministische Sperrvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fc24c0b503ec23d20be414508371c5e1f63e93d3b009a42e84d742e5f014c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927640"
---
# <a name="opportunistic-lock-operations"></a>Deterministische Sperrvorgänge

Wenn eine Anwendung mithilfe der [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mit dem **Flag FILE FLAG \_ \_ OVERLAPPED** für überlappende (asynchrone) Eingaben und Ausgaben geöffnet werden muss, müssen alle Dateien, für die sie Sperren an fordert, geöffnet werden. Nachdem die Dateien für den überlappenden Vorgang geöffnet wurden, können Sie die [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit einem der folgenden Steuerungscodes verwenden, um mit den deterministischen Sperren dieser Dateien zu arbeiten:

<dl>

[**FSCTL \_ OPBATCH \_ ACK \_ CLOSE \_ PENDING**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**FSCTL \_ OPLOCK \_ BREAK \_ ACK NO \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**FSCTL \_ OPLOCK \_ BREAK \_ ACKNOWLEDGE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**FSCTL \_ OPLOCK \_ BREAK \_ NOTIFY**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**FSCTL \_ REQUEST \_ BATCH \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**FSCTL \_ REQUEST \_ FILTER \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**FSCTL \_ REQUEST \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**FSCTL \_ REQUEST \_ OPLOCK LEVEL \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**FSCTL \_ REQUEST \_ OPLOCK LEVEL \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
