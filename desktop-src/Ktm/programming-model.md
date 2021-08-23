---
description: Anwendungsautoren können geringfügige Änderungen am Quellcode vornehmen, um mithilfe des KernelTransaktions-Managers (KTM) transaktive Datei- und Registrierungsvorgänge hinzuzufügen.
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: Arbeiten mit Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda967e3c8fe165c3a59de6534c26bc125dfb8dd209be68b5914ea099b0023e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146513"
---
# <a name="working-with-transactions"></a>Arbeiten mit Transaktionen

Anwendungsautoren können geringfügige Änderungen am Quellcode vornehmen, um mithilfe des KernelTransaktions-Managers (KTM) transaktive Datei- und Registrierungsvorgänge hinzuzufügen. In der Regel umfasst dies das Erstellen einer Transaktion und das Übergeben des Handles an andere Funktionen, die von Transaktionsressourcen wie [Transaktional NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) und der Transacted Registry bereitgestellt werden.

KTM bietet Mechanismen, damit Ihre Anwendung an Transaktionen teilnehmen und Ihren eigenen Transaktionsressourcen-Manager schreiben kann. Es gibt Funktionen, mit denen Sie vier Klassen von Kernelobjekten erstellen, verwalten und verwenden können: Transaktionen, Transaktions-Manager, Ressourcen-Manager und Eintragungen. Wenn Sie nur Transaktionen verwenden, müssen Sie nur mit Transaktionsobjekten arbeiten und diese Funktionen verwenden:

-   [**Createtransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**Committransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

Gehen Sie nie davon aus, dass eine Transaktion aktiv ist. Für Transaktionen kann ein Rollback aus vielen Gründen und jederzeit möglich sein.

Windows macht eine handlebasierte Schnittstelle für Systemressourcen verfügbar. Um mit einem Betriebssystemobjekt zu arbeiten, fordert die Anwendung zunächst ein Handle für das Objekt an und verwendet dieses Handle dann in nachfolgenden Funktionsaufrufen, um auf das Objekt zu zugreifen oder es zu ändern. Ein Handle kann in der Regel in verschiedenen Modi geöffnet werden. Der angegebene Modus wirkt sich auf die Semantik nachfolgender Funktionsaufrufe aus. Beispielsweise kann ein Dateihandles, das durch einen Aufruf von [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) geöffnet wird und das *flag dwDesiredAccess* auf **GENERIC \_ READ** festgelegt ist, nicht in Aufrufen verwendet werden, die die Datei ändern.

Sie können sich mit [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) Benutzermodusressourcen wie SQL oder MSMQ und mit Ressourcen im Kernelmodus, die KTM verwenden, koordinieren. Erstellen Sie zunächst eine DTC-Transaktion oder ein [**System.Transactions-Objekt,**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) und rufen Sie dann das [**IKernelTransaction-Objekt**](/previous-versions/windows/desktop/aa344210(v=vs.85)) auf, aus dem Sie das KTM-Handle abrufen können. Das **IKernelTransaction-Objekt** erstellt eine KTM-Transaktion, die der DTC-Transaktion untergeordnet ist. Mit diesem Handle können Sie Ihre transaktiven Objekte erstellen, aber das Ergebnis der Transaktion mithilfe von DTC oder **System.Transactions signalisieren.**

 

 
