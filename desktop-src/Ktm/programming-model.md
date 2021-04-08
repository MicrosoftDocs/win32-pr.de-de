---
description: Anwendungs Schreiber können kleinere Quell Codeänderungen vornehmen, um transaktive Datei-und Registrierungs Vorgänge mithilfe des Kerneltransaktions-Managers (KTM) hinzuzufügen.
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: Arbeiten mit Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255e40fb38ca4bfb24acdce717f133dbcf0c76f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865772"
---
# <a name="working-with-transactions"></a>Arbeiten mit Transaktionen

Anwendungs Schreiber können kleinere Quell Codeänderungen vornehmen, um transaktive Datei-und Registrierungs Vorgänge mithilfe des Kerneltransaktions-Managers (KTM) hinzuzufügen. In der Regel umfasst dies das Erstellen einer Transaktion und das Übergeben des Handles an andere Funktionen, die von Transaktions Ressourcen bereitgestellt werden, z. b. [Transaktions-NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) und die transaktive Registrierung.

KTM bietet Mechanismen, mit denen Ihre Anwendung an Transaktionen teilnehmen und ihren eigenen transaktionalen Ressourcen-Manager schreiben muss. Es gibt Funktionen, die es Ihnen ermöglichen, vier Klassen von Kernel Objekten zu erstellen, zu verwalten und mit Ihnen zu arbeiten: Transaktionen, Transaktions-Manager, Ressourcen-Manager und Eintragung. Wenn Sie einfach Transaktionen verwenden, müssen Sie nur mit Transaktions Objekten arbeiten und diese Funktionen verwenden:

-   [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

Gehen Sie niemals davon aus, dass eine Transaktion aktiv ist. Für Transaktionen kann aus vielen Gründen und jederzeit ein Rollback ausgeführt werden.

Windows macht eine Handle-basierte Schnittstelle für Systemressourcen verfügbar. Um mit einem Betriebssystem Objekt zu arbeiten, fordert die Anwendung zuerst ein Handle für das Objekt an und verwendet dann dieses Handle in nachfolgenden Funktionsaufrufen, um auf das Objekt zuzugreifen oder es zu ändern. Ein Handle kann normalerweise in unterschiedlichen Modi geöffnet werden. der angegebene Modus wirkt sich auf die Semantik von nachfolgenden Funktionsaufrufen aus. Beispielsweise kann ein Datei Handle, das durch einen Aufruf von " [**deatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " geöffnet wird, mit dem " *dwDesiredAccess* "-Flag, das auf " **generischer \_ Lese** Vorgang" festgelegt ist, nicht in Aufrufen verwendet werden,

Sie können mit [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) Benutzermodus-Ressourcen wie SQL oder MSMQ und mit kernelmodusressourcen, die KTM verwenden, koordinieren. Erstellen Sie zunächst eine DTC-Transaktion oder ein [**System. Transactions**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) -Objekt, und rufen Sie dann das [**IKernelTransaction**](/previous-versions/windows/desktop/aa344210(v=vs.85)) -Objekt auf, von dem Sie den KTM-handle abrufen können. Das **IKernelTransaction** -Objekt erstellt eine KTM-Transaktion, die der DTC-Transaktion untergeordnet ist. Mit diesem Handle können Sie die transaktiven Objekte erstellen, aber das Ergebnis der Transaktion mithilfe von DTC oder **System. Transactions** signalisieren.

 

 
