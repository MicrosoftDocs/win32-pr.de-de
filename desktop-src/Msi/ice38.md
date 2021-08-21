---
description: ICE38 überprüft, ob jede Komponente, die unter dem Profil des aktuellen Benutzers installiert wird, auch einen Registrierungsschlüssel unter dem Stamm HKEY \_ CURRENT USER in der \_ KeyPath-Spalte der Tabelle Component angibt.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3f90b7f6c0624da266b23dee3a50489f34604d6c99783b337eeca77bb32ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528460"
---
# <a name="ice38"></a>ICE38

ICE38 überprüft, ob jede Komponente, die unter dem Profil des aktuellen Benutzers installiert wird, auch einen Registrierungsschlüssel unter dem **Stamm HKEY \_ CURRENT \_ USER** in der KeyPath-Spalte der [Tabelle Component](component-table.md)angibt.

## <a name="result"></a>Ergebnis

ICE38 sendet einen Fehler, wenn eine Komponente, die unter dem Profil des Benutzers installiert ist, keinen HKCU-Registrierungsschlüssel angibt.

## <a name="example"></a>Beispiel

ICE38 meldet die folgenden Fehler für das gezeigte Beispiel.



| ICE38-Fehler                                                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Component Component1 wird im Benutzerprofil installiert. Es muss einen Registrierungsschlüssel unter HKCU als KeyPath und keine Datei verwenden.                    | Der Wert der Attributspalte von Component1 ist 0, was bedeutet, dass die Komponente eine Datei als KeyPath verwenden muss. Dies führt zu Problemen, wenn mehrere Benutzer die Komponente auf demselben Computer installieren. Um diesen Fehler auf Component1 zu beheben, legen Sie das RegistryKeyPath-Bit in der Attributes -Spalte der [Component-Tabelle](component-table.md) fest, und ändern Sie den Eintrag in der KeyPath-Spalte in einen Wert, der in der Spalte Registrierung der [Registrierungstabelle](registry-table.md)aufgeführt ist.<br/>                                                                                |
| Component Component2 wird im Benutzerprofil installiert. Es muss einen Registrierungsschlüssel unter HKCU als KeyPath verwenden. KeyPath ist derzeit NULL. | Für Component2 ist das RegistryKeyPath-Bit in der Attributes -Spalte der [Component-Tabelle](component-table.md)festgelegt. Das Feld KeyPath muss daher einen Schlüssel für die Spalte Registry der [Registrierungstabelle](registry-table.md) enthalten, aber die KeyPath-Spalte ist NULL. Um diesen Fehler zu beheben, ändern Sie den KeyPath-Wert in einen gültigen Eintrag in der Registrierungstabelle.<br/>                                                                                                                                                                                                     |
| Komponente Component3 wird im Benutzerprofil installiert. Der KeyPath-Registrierungsschlüssel muss unter HKCU fallen.                                      | Für Component3 ist das RegistryKeyPath-Bit in der Attributes -Spalte der [Component-Tabelle](component-table.md) festgelegt, aber der Stamm des Registrierungseintrags, der in der Stammspalte der Registrierungstabelle angegeben ist, gibt **HKEY \_ LOCAL \_ MACHINE** anstelle von **HKEY \_ CURRENT \_ USER** an. Um diesen Fehler zu beheben, verwenden Sie einen gültigen Registrierungseintrag unter **HKEY \_ LOCAL \_ MACHINE** als KeyPath für diese Komponente, oder ändern Sie den Wert in der Stammspalte der [Registrierungstabelle](registry-table.md) in -1 oder 1.<br/>                                                                  |
| Der KeyPath-Registrierungseintrag für komponente Component4 ist nicht vorhanden.                                                                 | Für Component4 ist das RegistryKeyPath-Bit in der Attributes -Spalte der [Component-Tabelle](component-table.md) festgelegt, aber der Eintrag in der KeyPath-Spalte ist in der [Registrierungstabelle](registry-table.md)nicht vorhanden. Um diesen Fehler zu beheben, fügen Sie der Registrierungstabelle einen Eintrag für Reg4 hinzu, der unter **HKEY \_ CURRENT \_ USER** ein ist.<br/>                                                                                                                                                                                                                                      |
| Der Registrierungseintrag Reg5 wird als KeyPath für die Komponente Component5 festgelegt, aber dieser Registrierungseintrag gehört nicht zu Component5.      | Der Registrierungseintrag, auf den in der KeyPath-Spalte der Komponente verwiesen wird, wurde gefunden und befindet sich unter der HKCU-Struktur. Die Spalte Komponente des Registrierungseintrags verweist jedoch \_ nicht auf dieselbe Komponente, die sie als KeyPathauflistet hat. Dies bedeutet, dass der Registrierungseintrag, der als KeyPath der Komponente verwendet wird, nur erstellt wird, wenn eine andere Komponente installiert wurde. Um diesen Fehler zu beheben, ändern Sie den KeyPath-Wert so, dass er auf einen Registrierungseintrag verweist, der zur Komponente gehört, oder ändern Sie den Registrierungseintrag so, dass er zur Komponente gehört, indem Sie ihn als KeyPath verwenden.<br/> |



 

[Verzeichnistabelle](directory-table.md) (partiell)



| Verzeichnis | \_Übergeordnetes Verzeichnis | DefaultDir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | StartMenuFolder |
| Dir2      |                   | DesktopFolder   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | Subdir          |



 

[Komponententabelle](component-table.md) (teilweise)



| Komponente  | Verzeichnis\_ | Attribute | KeyPath |
|------------|-------------|------------|---------|
| Komponente1 | Dir1        | 0          | Datei1   |
| Component2 | Dir2        | 4          |         |
| Component3 | Dir3        | 4          | Reg3    |
| Komponente4 | Dir4        | 4          | Reg4    |
| Komponente5 | Dir5        | 4          | Reg5    |



 

[Registrierungstabelle](registry-table.md) (partiell)



| Registry | Root | Wert | Komponente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Komponente4  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




