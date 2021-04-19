---
description: Befolgen Sie die allgemeinen Richtlinien zum Anwenden von Mergemodulen, die unter Anwenden von Mergemodulen
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Anwenden eines konfigurierbaren Mergemoduls mit Anpassungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360220"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>Anwenden eines konfigurierbaren Mergemoduls mit Anpassungen

Befolgen Sie die allgemeinen Richtlinien zum Anwenden von Mergemodulen, die unter [Anwenden von Mergemodulen](applying-merge-modules.md) Außerdem müssen mergemodulconsumer folgende Schritte ausführen, um ein Mergemodul zum Zeitpunkt der Installation zu konfigurieren:

-   Verwenden Sie ein Mergemodul, das erstellt wurde, um konfigurierbare Einstellungen zu haben. Weitere Informationen finden Sie unter [Erstellen eines Mergemoduls, das vom Endbenutzer konfiguriert werden kann](creating-a-merge-module-that-can-be-configured-by-the-end-user.md) .
-   Verwenden Sie ein Merge-und Konfigurationstool, das Mergemod.dll-Version 2,0 oder höher aufruft. In früheren Versionen von Mergmod.dll können die mergemoduleinstellungen nicht konfiguriert werden. Autoren sollten Mergemodule erstellen, die Standardwerte bereitstellen und mit früheren Versionen von Mergmod.dll kompatibel sind.
-   Geben Sie Anpassungs Informationen an, wenn Sie vom Konfigurations Client Tool dazu aufgefordert werden. Autoren sollten Mergemodule erstellen, die Standardwerte verwenden, wenn ein Benutzer die Angabe von Informationen ablehnt.

 

 



