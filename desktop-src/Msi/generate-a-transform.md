---
description: Die VBScript-Datei WiGenXfm.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispielskript kann eine Transformation aus zwei Windows Installer-Datenbanken generieren. Weitere Informationen finden Sie unter Daten Bank Transformationen.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Generieren einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757644"
---
# <a name="generate-a-transform"></a>Generieren einer Transformation

Die VBScript-Datei WiGenXfm.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispielskript kann eine Transformation aus zwei Windows Installer-Datenbanken generieren. Weitere Informationen finden Sie unter [Daten Bank Transformationen](database-transforms.md).

Das Beispiel veranschaulicht die Verwendung von:

[**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)

[**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)

[**GenerateTransform-Methode**](database-generatetransform.md) des [ **Datenbankobjekts**](database-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiGenXfm.vbs \[ Pfad zum ursprünglichen Daten Bank Pfad \] \[ zum überarbeiteten Daten Bank \] \[ Pfad zur Transformations Datei\]**

Geben Sie den Pfad zur ursprünglichen Windows Installer Datenbank an. Geben Sie den Pfad zur überarbeiteten Datenbank an. Geben Sie den Pfad zu der zu erstellenden Transformations Datei an. Wenn der Pfad zur Transformations Datei weggelassen wird, werden die beiden Datenbanken nur verglichen.

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

Beachten Sie, dass [ein Lokalisierungs Beispiel](a-localization-example.md) das [Erstellen einer Anpassungs Transformation](generating-a-customization-transform.md)veranschaulicht.

 

 



