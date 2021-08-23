---
description: ICE80 überprüft, ob der Wert der Template Summary Property (PID TEMPLATE) ordnungsgemäß \_ &\# 0034;Intel64&\# 0034;, &\# 0034;x64&\# 0034; oder &\# 0034;Intel&0034; angibt, je nachdem, ob \# 64-Bit-Komponenten oder benutzerdefinierte Aktionsskripts vorliegen.
ms.assetid: fd2a15cf-d117-4a87-a26e-caff4b12a2e9
title: ICE80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7be298e406db40b76a54eadbe12e99175e0058d97c4d57c5a4b1cd842b000f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339940"
---
# <a name="ice80"></a>ICE80

ICE80 überprüft, ob der Wert der [**Template Summary**](template-summary.md) Property (PID \_ TEMPLATE) "Intel64", "x64", "Arm64" oder "Intel" richtig angibt, je nachdem, ob 64-Bit-Komponenten oder benutzerdefinierte Aktionsskripts vorliegen. ICE80 überprüft die [Komponententabelle](component-table.md) auf Komponenten mit dem **Attribut msidbComponentAttributes64bit** und überprüft die [CustomAction-Tabelle](customaction-table.md) auf Skripts mit dem **Attribut msidbCustomActionType64BitScript.** ICE80 überprüft, ob ein Paket mit "Intel64", "x64" oder  "Arm64" [](page-count-summary.md) in der Zusammenfassungseigenschaft der Vorlage auch über eine Zusammenfassungseigenschaft der Seitenanzahl (PAGECOUNT) von mindestens \_ 150 verfügt.

ICE80 überprüft auch, ob die von der [**ProductLanguage-Eigenschaft**](productlanguage.md) angegebene Sprach-ID in der [**Template Summary Property enthalten sein**](template-summary.md) muss.

Weitere Informationen finden Sie unter [Windows Installer unter 64-Bit-Betriebssystemen.](windows-installer-on-64-bit-operating-systems.md)

## <a name="result"></a>Ergebnis

ICE80 veröffentlicht die folgenden Fehler.



| Fehler                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dieses Paket enthält die 64-Bit-Komponente "1", aber die Eigenschaft "Vorlagenzusammenfassung" enthält \[ \] nicht Intel64, x64 oder Arm64. [](template-summary.md)                    | Die [Komponententabelle](component-table.md)enthält eine Komponente mit dem **Attribut msidbComponentAttributes64bit,** und die Eigenschaft für die Vorlagenzusammenfassung enthält intel64, x64 oder Arm64 nicht. [](template-summary.md)        |
| Dieses Paket enthält das benutzerdefinierte 64-Bit-Aktionsskript "1", aber die Eigenschaft "Vorlagenzusammenfassung" enthält \[ \] nicht Intel64, x64 oder Arm64. [](template-summary.md)         | [Die CustomAction-Tabelle](customaction-table.md) enthält eine benutzerdefinierte Skriptaktion mit **msidbCustomActionType64BitScript,** aber die Zusammenfassungseigenschaft der Vorlage enthält nicht Intel64, x64 oder Arm64. [](template-summary.md) |
| Fehlerhafter Wert im Zusammenfassungsinformationsstream für %s.                                                                                                                         | Wird für die PID \_ TEMPLATE-Eigenschaft zurückgegeben, wenn diese Eigenschaft eine leere Zeichenfolge oder kein VT \_ LPSTR-Typ ist. Wird für PID \_ PAGECOUNT zurückgegeben, wenn diese Eigenschaft kein VT \_ I4-Typ ist.<br/>                                         |
| Dieses Paket ist mit Intel64 gekennzeichnet, verfügt aber über ein Schema kleiner als 150.                                                                                                  | Die PID \_ TEMPLATE-Eigenschaft des Pakets ist Intel64, aber die PID \_ PAGECOUNT-Eigenschaft ist kleiner als 150.                                                                                                            |
| Dieses Paket ist mit x64 gekennzeichnet, verfügt aber über ein Schema kleiner als 200.                                                                                                      | Die PID \_ TEMPLATE-Eigenschaft des Pakets ist x64, aber die PID \_ PAGECOUNT-Eigenschaft ist kleiner als 200.                                                                                                            |
| Dieses Paket ist mit Arm64 markiert, verfügt aber über ein Schema kleiner als 500.                                                                                                    | Die PID \_ TEMPLATE-Eigenschaft des Pakets ist Arm64, aber die PID \_ PAGECOUNT-Eigenschaft ist kleiner als 500.                                                                                                            |
| Dieses 32-Bit-Paket verwendet die 64-Bit-Eigenschaft \[ 1.\]                                                                                                                       | Ein 32-Bit-Paket verwendet eine 64-Bit-Eigenschaft.                                                                                                                                                                              |
| Dieses 32-Bit-Paket verwendet den 64-Bit-Locatortyp im RegLocator-Tabelleneintrag \[ 1.\]                                                                                         | Ein 32-Bit-Paket enthält **msidbLocatorType64bit** im Feld Typ der [RegLocator-Tabelle](reglocator-table.md).                                                                                                    |
| Diese 64BitComponent \[ 1 verwendet \] 32BitDirectory \[ 3.\]                                                                                                                     | Eine 64-Bit-Komponente verwendet ein 32-Bit-Verzeichnis.                                                                                                                                                                           |
| Diese 32BitComponent \[ 1 verwendet \] 64BitDirectory \[ 3.\]                                                                                                                     | Eine 32-Bit-Komponente verwendet ein 64-Bit-Verzeichnis.                                                                                                                                                                           |
| Die [**ProductLanguage-Eigenschaft**](productlanguage.md)in der Property-Tabelle hat den Wert ' 2 ', der nicht im Template \[ \] Summary Property-Stream enthalten ist. | Der Wert der [**ProductLanguage-Eigenschaft**](productlanguage.md) ist nicht in der [**Eigenschaft Vorlagenzusammenfassung**](template-summary.md) aufgeführt.                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> <dt>

[Windows Installationsprogramm unter 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md)
</dt> </dl>

 

 




