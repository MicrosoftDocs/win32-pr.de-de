---
description: Die VBScript-Datei WiGenXfm.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt. Dieses Beispielskript kann eine Transformation aus zwei Windows Installer-Datenbanken generieren. Weitere Informationen finden Sie unter Datenbanktransformationen.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Generieren einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba16c894ec32bf300f1572eb26311be70315872b9711ca46573ce65e18802308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142767"
---
# <a name="generate-a-transform"></a>Generieren einer Transformation

Die VBScript-Datei WiGenXfm.vbs wird in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispielskript kann eine Transformation aus zwei Windows Installer-Datenbanken generieren. Weitere Informationen finden Sie unter [Datenbanktransformationen.](database-transforms.md)

Das Beispiel veranschaulicht die Verwendung von:

[**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)

[**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)

[**GenerateTransform-Methode**](database-generatetransform.md) des [ **Database-Objekts**](database-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Um CScript.exe zum Ausführen dieses Beispiels zu verwenden, geben Sie eine Befehlszeile an der Eingabeaufforderung mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn die Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiGenXfm.vbs \[ Pfad zum ursprünglichen \] \[ Datenbankpfad zum überarbeiteten \] \[ Datenbankpfad zum Transformieren der Datei\]**

Geben Sie den Pfad zur ursprünglichen Windows Installer-Datenbank an. Geben Sie den Pfad zur überarbeiteten Datenbank an. Geben Sie den Pfad zur zu erstellenden Transformationsdatei an. Wenn der Pfad zur Transformationsdatei weggelassen wird, werden die beiden Datenbanken nur verglichen.

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielhilfsprogramme, die Windows Script Host nicht benötigen, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

Beachten Sie, dass [ein Lokalisierungsbeispiel](a-localization-example.md) das [Generieren einer Anpassungstransformation](generating-a-customization-transform.md)veranschaulicht.

 

 



