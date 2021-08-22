---
description: Befolgen Sie die allgemeinen Richtlinien zum Anwenden von Mergemodulen, die unter Anwenden von Mergemodulen beschrieben sind.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Anwenden eines konfigurierbaren Mergemoduls mit Anpassungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e9c771493a7a8e854472d840ffc21358c9741d8b3a8ea9876251456b6badf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829200"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>Anwenden eines konfigurierbaren Mergemoduls mit Anpassungen

Befolgen Sie die allgemeinen Richtlinien zum Anwenden von Mergemodulen, die unter [Anwenden von Mergemodulen](applying-merge-modules.md)beschrieben sind. Darüber hinaus müssen Mergemodul-Consumer folgende Schritte ausführen, um ein Mergemodul zum Zeitpunkt der Installation zu konfigurieren:

-   Verwenden Sie ein Mergemodul, das für konfigurierbare Einstellungen erstellt wurde. Weitere Informationen finden Sie unter [Erstellen eines Mergemoduls, das vom Endbenutzer konfiguriert werden kann.](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)
-   Verwenden Sie ein Merge- und Konfigurationstool, das Mergemod.dll Version 2.0 oder höher aufruft. Frühere Versionen von Mergmod.dll können keine Mergemoduleinstellungen konfigurieren. Autoren sollten Mergemodule erstellen, die Standardwerte bereitstellen und mit früheren Versionen von Mergmod.dll kompatibel sind.
-   Geben Sie Anpassungsinformationen an, wenn Sie vom Konfigurationsclienttool dazu aufgefordert werden. Autoren sollten Mergemodule erstellen, die Standardwerte verwenden, wenn ein Benutzer die Bereitstellung von Informationen ablehnt.

 

 



