---
description: ICE38 überprüft, ob jede Komponente, die unter dem Profil des aktuellen Benutzers installiert wird, auch einen Registrierungsschlüssel unter dem aktuellen HKEY- \_ \_ Benutzer Stamm in der KEYPATH-Spalte der Komponenten Tabelle angibt.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d001d244160f939a73e697e677bf43a1f5f825f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042535"
---
# <a name="ice38"></a>ICE38

ICE38 überprüft, ob jede Komponente, die unter dem Profil des aktuellen Benutzers installiert wird, auch einen Registrierungsschlüssel unter dem **aktuellen HKEY- \_ \_ Benutzer** Stamm in der KEYPATH-Spalte der [Komponenten Tabelle](component-table.md)angibt.

## <a name="result"></a>Ergebnis

ICE38 gibt einen Fehler aus, wenn eine Komponente, die im Profil des Benutzers installiert ist, keinen HKCU-Registrierungsschlüssel angibt.

## <a name="example"></a>Beispiel

ICE38 meldet die folgenden Fehler für das angezeigte Beispiel.



| ICE38-Fehler                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Komponente Component1 wird in Benutzerprofil installiert. Dabei muss es sich um einen Registrierungsschlüssel unter HKCU als KEYPATH und nicht um eine Datei handelt.                    | Der Wert der Spalte Attribute von Component1 ist 0, was bedeutet, dass die Komponente eine Datei als KEYPATH verwenden muss. Dies verursacht Schwierigkeiten, wenn mehrere Benutzer die Komponente auf demselben Computer installieren. Legen Sie zum Beheben dieses Fehlers auf Component1 das registrykeypath-Bit in der Attribute-Spalte der [Component-Tabelle](component-table.md) fest, und ändern Sie den Eintrag in der KEYPATH-Spalte in einen Wert, der in der Registrierungs Spalte der [Registrierungs Tabelle](registry-table.md)aufgeführt ist.<br/>                                                                                |
| Komponente Component2 wird in Benutzerprofil installiert. Dabei muss ein Registrierungsschlüssel unter HKCU als KEYPATH verwendet werden. Der KEYPATH ist zurzeit NULL. | In Component2 ist das registrykeypath-Bit in der Attribute-Spalte der [Component-Tabelle](component-table.md)festgelegt. Das KEYPATH-Feld muss daher einen Schlüssel für die Registrierungs Spalte der [Registrierungs Tabelle](registry-table.md) enthalten, die KEYPATH-Spalte ist jedoch NULL. Um diesen Fehler zu beheben, ändern Sie den Wert für KEYPATH in einen gültigen Eintrag in die Registrierungs Tabelle.<br/>                                                                                                                                                                                                     |
| Komponente Component3 wird in Benutzerprofil installiert. Der KEYPATH-Registrierungsschlüssel muss unter HKCU liegen.                                      | In Component3 ist das registrykeypath-Bit in der Attribute-Spalte der [Component-Tabelle](component-table.md) festgelegt, aber der Stamm des Registrierungs Eintrags, der in der root-Spalte der Registrierungs Tabelle angegeben ist, gibt den **lokalen HKEY- \_ \_ Computer** anstelle des **aktuellen HKEY- \_ \_ Benutzers** an. Um diesen Fehler zu beheben, verwenden Sie einen gültigen Registrierungs Eintrag unter **HKEY \_ local \_ Machine** als KEYPATH für diese Komponente, oder ändern Sie den Wert in der Spalte root der [Registrierungs Tabelle](registry-table.md) in-1 oder 1.<br/>                                                                  |
| Der KEYPATH-Registrierungs Eintrag für die Komponente Component4 ist nicht vorhanden.                                                                 | In Component4 ist das registrykeypath-Bit in der Attribute-Spalte der [Component-Tabelle](component-table.md) festgelegt, aber der Eintrag in der KEYPATH-Spalte ist in der [Registrierungs Tabelle](registry-table.md)nicht vorhanden. Um diesen Fehler zu beheben, fügen Sie der Registrierungs Tabelle einen Eintrag für Reg4 hinzu, bei dem es sich um einen unter **HKEY \_ Current \_ User** handelt.<br/>                                                                                                                                                                                                                                      |
| Der Registrierungs Eintrag Reg5 wird als KEYPATH für die Komponente Component5 festgelegt, aber dieser Registrierungs Eintrag gehört nicht zu Component5.      | Der Registrierungs Eintrag, auf den in der KEYPATH-Spalte der Komponente verwiesen wird, wurde gefunden und befindet sich unter der HKCU-Struktur, aber die Komponenten Spalte des Registrierungs Eintrags \_ verweist nicht auf dieselbe Komponente, die Sie als KEYPATH aufgelistet hat. Dies bedeutet, dass der Registrierungs Eintrag, der als KEYPATH der Komponente verwendet wird, nur dann erstellt wird, wenn eine andere Komponente installiert wurde. Um diesen Fehler zu beheben, ändern Sie den KEYPATH-Wert so, dass er auf einen Registrierungs Eintrag verweist, der zur Komponente gehört, oder ändern Sie den Registrierungs Eintrag so, dass er zur Komponente gehört, indem er ihn als KEYPATH verwendet.<br/> |



 

[Verzeichnis Tabelle](directory-table.md) (partiell)



| Verzeichnis | Über \_ geordnetes Verzeichnis | DefaultDir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | Startmenü Ordner |
| Dir2      |                   | DesktopFolder   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | SubDir          |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | Verzeichnis\_ | Attribute | KEYPATH |
|------------|-------------|------------|---------|
| Component1 | Dir1        | 0          | Datei1   |
| Component2 | Dir2        | 4          |         |
| Component3 | Dir3        | 4          | Reg3    |
| Component4 | Dir4        | 4          | Reg4    |
| Component5 | Dir5        | 4          | Reg5    |



 

[Registrierungs Tabelle](registry-table.md) (partiell)



| Registrierung | Root | Wert | Komponente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




