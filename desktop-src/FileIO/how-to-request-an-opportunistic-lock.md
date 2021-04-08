---
description: Opportunistische Sperren werden angefordert, indem zuerst eine Datei mit Berechtigungen und Flags geöffnet wird, die für die Anwendung geeignet sind, die die Datei öffnet. Alle Dateien, für die opportunistische Sperren angefordert werden, müssen für einen überlappenden (asynchronen) Vorgang geöffnet werden.
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Anfordern einer opportunistischen Sperre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868239"
---
# <a name="how-to-request-an-opportunistic-lock"></a>Anfordern einer opportunistischen Sperre

Client Anwendungen fordern opportunistische Sperren direkt an, wenn die Sperre für eine Datei auf dem lokalen Server vorgesehen ist. Beim Zugriff auf Dateien auf Remote Servern ist dies der Netzwerkredirector und nicht die Client Anwendung, die die opportunistische Sperre vom Remote Server anfordert.

Opportunistische Sperren werden angefordert, indem zuerst eine Datei mit Berechtigungen und Flags geöffnet wird, die für die Anwendung geeignet sind, die die Datei öffnet. Alle Dateien, für die opportunistische Sperren angefordert werden, müssen für einen überlappenden (asynchronen) Vorgang geöffnet werden. Nachdem die Dateien für einen überlappenden Vorgang geöffnet wurden, verwenden Sie die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion mit dem entsprechenden Steuerungs Code, um eine opportunistische Sperre anzufordern. Eine Liste der opportunistischen Lock-Vorgänge finden Sie unter [opportunistische Lock-Vorgänge](opportunistic-lock-operations.md).

Anwendungen werden benachrichtigt, dass eine opportunistische Sperre mit dem **hevent** -Member der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur, die der Datei zugeordnet ist, beschädigt wird. Anwendungen können auch Funktionen wie [**gedeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) und [**hasoverlappedioabgeschlossene**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted)verwenden. Die Anwendung ist dafür verantwortlich, die richtige Datei mit der unterbrochenen opportunistischen Sperre zu verknüpfen.

Weitere Informationen zur Benachrichtigung finden Sie unter [Synchronisierung](/windows/desktop/Sync/synchronization).

 

 
