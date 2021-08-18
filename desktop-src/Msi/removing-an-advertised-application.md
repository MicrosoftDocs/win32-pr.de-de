---
description: Um eine Anwendung zu entfernen, die im angekündigten Zustand installiert wurde, deinstallieren Sie sie einfach mit MsiInstallProduct oder MsiConfigureProduct. Sie können eine angekündigte Anwendung auch aus der Befehlszeile entfernen. Weitere Informationen finden Sie unter Befehlszeilenoptionen.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Entfernen einer angekündigten Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880ce7d7de7ce7a8f9c9a20511f3f9d1b48ccdf34ffd2da51a71d226d0770b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041580"
---
# <a name="removing-an-advertised-application"></a>Entfernen einer angekündigten Anwendung

Um eine Anwendung zu entfernen, die im angekündigten Zustand installiert wurde, deinstallieren Sie sie einfach mit [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) oder [**MsiConfigureProduct.**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) Sie können eine angekündigte Anwendung auch aus der Befehlszeile entfernen. Weitere Informationen finden Sie unter [Befehlszeilenoptionen.](command-line-options.md)

Beachten Sie, dass Sie eine angekündigte Anwendung möglicherweise nicht entfernen können, wenn Sie das Paket so erstellt haben, dass die Ausführung einer Installation von der Anweisung **NICHT installiert** abhängig ist. Eine angekündigte Anwendung wird nicht auf dem Computer des Benutzers installiert, und das Installationsprogramm legt die [**Installierte**](installed.md) Eigenschaft nicht fest. Das Paket muss erstellt werden, damit angekündigte Anwendungen deinstalliert werden können.

 

 



