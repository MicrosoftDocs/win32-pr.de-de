---
description: ICE80 überprüft, ob der Wert der Template Summary-Eigenschaft (PID- \_ Vorlage) korrekt &\# 0034; Intel64&\# 0034;, &\# 0034; x64&\# 0034; oder &\# 0034; Intel&\# 0034; angibt, je nachdem, ob 64-Bit-Komponenten oder benutzerdefinierte Aktions Skripts vorhanden sind.
ms.assetid: fd2a15cf-d117-4a87-a26e-caff4b12a2e9
title: ICE80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5233f260e9cc248bdb2d0c19b47956a2b7dbe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356815"
---
# <a name="ice80"></a>ICE80

ICE80 überprüft, ob der Wert der [**Template Summary**](template-summary.md) -Eigenschaft (PID \_ -Vorlage) ordnungsgemäß "Intel64", "x64", "Arm64" oder "Intel" angibt, je nachdem, ob 64-Bit-Komponenten oder benutzerdefinierte Aktions Skripts vorhanden sind. ICE80 überprüft die Komponenten [Tabelle](component-table.md) auf alle Komponenten mit dem **msidbComponentAttributes64bit** -Attribut und überprüft die [CustomAction-Tabelle](customaction-table.md) auf alle Skripts mit dem **msidbCustomActionType64BitScript** -Attribut. ICE80 überprüft, ob ein Paket mit "Intel64", "x64" oder "Arm64" in der **Vorlagen Zusammenfassungs** Eigenschaft auch eine [**Zusammenfassungs Eigenschaft der Seitenanzahl**](page-count-summary.md) (PID \_ Page count) von mindestens 150 hat.

ICE80 überprüft auch, ob die von der [**productlanguage**](productlanguage.md) -Eigenschaft angegebene Sprach-ID in der [**Template-Übersichts**](template-summary.md) Eigenschaft enthalten sein muss.

Weitere Informationen finden Sie unter [Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md).

## <a name="result"></a>Ergebnis

ICE80 gibt die folgenden Fehler aus.



| Fehler                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dieses Paket enthält die 64-Bit-Komponente ' \[ 1 \] ', die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft enthält jedoch nicht Intel64, x64 oder Arm64.                    | Die [Komponenten Tabelle](component-table.md)enthält eine Komponente mit dem **msidbComponentAttributes64bit** -Attribut, und die [**Template Summary**](template-summary.md) -Eigenschaft enthält nicht Intel64, x64 oder Arm64.        |
| Dieses Paket enthält ein benutzerdefiniertes 64-Bit-Aktions Skript ' \[ 1 \] ', aber die [**Template Summary**](template-summary.md) -Eigenschaft enthält nicht Intel64, x64 oder Arm64.         | Die [CustomAction-Tabelle](customaction-table.md) enthält eine benutzerdefinierte Skript Aktion mit **msidbCustomActionType64BitScript** , aber die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft enthält nicht Intel64, x64 oder Arm64. |
| Ungültiger Wert im Zusammenfassungs Informationsdaten Strom für% s.                                                                                                                         | Wird für die PID- \_ Vorlagen Eigenschaft zurückgegeben, wenn diese Eigenschaft eine leere Zeichenfolge oder kein VT \_ LPSTR-Typ ist. Wird für PID \_ Page count zurückgegeben, wenn diese Eigenschaft kein VT \_ I4 Type ist.<br/>                                         |
| Dieses Paket ist mit Intel64 gekennzeichnet, hat jedoch ein Schema, das kleiner als 150 ist.                                                                                                  | Die PID- \_ Vorlagen Eigenschaft des Pakets ist Intel64, die PID \_ Page Count-Eigenschaft ist jedoch kleiner als 150.                                                                                                            |
| Dieses Paket ist mit x64 gekennzeichnet, hat aber ein Schema, das kleiner als 200 ist.                                                                                                      | Die PID- \_ Vorlagen Eigenschaft des Pakets ist x64, die PID \_ Page Count-Eigenschaft ist jedoch kleiner als 200.                                                                                                            |
| Dieses Paket ist mit Arm64 gekennzeichnet, hat jedoch ein Schema, das kleiner als 500 ist.                                                                                                    | Die PID- \_ Vorlagen Eigenschaft des Pakets ist Arm64, die PID \_ Page Count-Eigenschaft ist jedoch kleiner als 500.                                                                                                            |
| Dieses 32-Bit-Paket verwendet die 64-Bit-Eigenschaft \[ 1.\]                                                                                                                       | Ein 32-Bit-Paket verwendet eine 64-Bit-Eigenschaft.                                                                                                                                                                              |
| Dieses 32-Bit-Paket verwendet den 64-Bit-Locatortyp in der reglocator-Tabelle \[ 1.\]                                                                                         | Ein 32-Bit-Paket enthält **msidbLocatorType64bit** im type-Feld der [reglocator-Tabelle](reglocator-table.md).                                                                                                    |
| Diese 64 bitcomponent \[ 1 \] verwendet 32 bitdirectory \[ 3\]                                                                                                                     | Eine 64-Bit-Komponente verwendet ein 32-Bit-Verzeichnis.                                                                                                                                                                           |
| Diese 32 bitcomponent \[ 1 \] verwendet 64 bitdirectory \[ 3\]                                                                                                                     | Eine 32-Bit-Komponente verwendet ein 64-Bit-Verzeichnis.                                                                                                                                                                           |
| Die [**productlanguage**](productlanguage.md)-Eigenschaft in der Eigenschaften Tabelle weist den Wert " \[ 2" auf \] , der nicht im Vorlagen Zusammenfassungs-Eigenschafts Datenstrom enthalten ist. | Der Wert der [**productlanguage**](productlanguage.md) -Eigenschaft ist nicht in der [**Template-Übersichts**](template-summary.md) Eigenschaft aufgeführt.                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> <dt>

[Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md)
</dt> </dl>

 

 




