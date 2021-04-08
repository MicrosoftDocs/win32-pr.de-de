---
description: Um eine Anwendung zu entfernen, die im angekündigten Zustand installiert wurde, deinstallieren Sie Sie einfach mithilfe von msiinstallproduct oder msikonfigurireproduct. Sie können eine angekündigte Anwendung auch über die Befehlszeile entfernen. Siehe Befehlszeilenoptionen.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Entfernen einer angekündigten Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866076"
---
# <a name="removing-an-advertised-application"></a>Entfernen einer angekündigten Anwendung

Um eine Anwendung zu entfernen, die im angekündigten Zustand installiert wurde, deinstallieren Sie Sie einfach mithilfe von [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) oder [**msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta). Sie können eine angekündigte Anwendung auch über die Befehlszeile entfernen. Siehe [Befehlszeilenoptionen](command-line-options.md).

Beachten Sie, dass es möglicherweise nicht möglich ist, eine angekündigte Anwendung zu entfernen, wenn Sie das Paket so verfasst haben, dass die Ausführung einer Installation von der Anweisung abhängt, die **nicht installiert** ist. Eine angekündigte Anwendung ist nicht auf dem Computer des Benutzers installiert, und die [**installierte**](installed.md) Eigenschaft wird vom Installationsprogramm nicht festgelegt. Das Paket muss erstellt werden, damit angekündigte Anwendungen deinstalliert werden können.

 

 



