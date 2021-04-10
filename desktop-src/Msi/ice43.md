---
description: ICE43 überprüft, ob Verknüpfungen, die nicht auf eine Funktion verweisen, als Ziel (nicht angekündigte Verknüpfungen) in Komponenten mit einem HKCU-Registrierungs Eintrag als Schlüssel Pfad vorhanden sind.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9df4a6051557fca3e185f56ca3ad7978c2c0b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131869"
---
# <a name="ice43"></a>ICE43

ICE43 überprüft, ob Verknüpfungen, die nicht auf eine Funktion verweisen, als Ziel (nicht angekündigte Verknüpfungen) in Komponenten mit einem HKCU-Registrierungs Eintrag als Schlüssel Pfad vorhanden sind.

## <a name="result"></a>Ergebnis

ICE43 gibt eine Fehlermeldung aus, wenn sich eine nicht angekündigte Verknüpfung in einer Komponente befindet, die keinen HKCU-Registrierungs Eintrag als Schlüssel Pfad hat.

## <a name="example"></a>Beispiel

ICE43 würde die folgenden Fehler für das gezeigte Beispiel melden.



| ICE43-Fehler                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Komponente Component1 enthält nicht angekündigte Verknüpfungen. Dabei muss es sich um einen Registrierungsschlüssel unter HKCU als KEYPATH und nicht um eine Datei handelt.                    | Die Attribute-Spalte von Component1 ist 0, was bedeutet, dass die Komponente eine Datei als KEYPATH verwendet. Dies bewirkt, dass nicht angekündigte Verknüpfungen in dieser Komponente nur für den ersten Benutzer auf dem Computer installiert werden. Benutzer, die die Komponente zu einem späteren Zeitpunkt installieren, sehen die Verknüpfungen nicht, da die Komponente dem Installer angezeigt wird, da Sie bereits auf dem Computer vorhanden ist. Legen Sie zum Beheben dieses Fehlers das registrykeypath-Bit der Attribute so fest, dass die Komponente in einen Registrierungs Eintrag wechselt, und ändern Sie dann den Wert von KEYPATH in einen gültigen Eintrag in der Registrierungs Tabelle.<br/> |
| Die Komponente Component2 enthält nicht angekündigte Verknüpfungen. Dabei muss ein Registrierungsschlüssel unter HKCU als KEYPATH verwendet werden. Der KEYPATH ist zurzeit NULL. | Die Attribute-Spalte ist auf die Verwendung der Registrierung festgelegt, aber der KEYPATH ist NULL. Der KEYPATH muss auf einen Eintrag in der Registrierungs Tabelle verweisen. Ändern Sie den Wert für KEYPATH in einen gültigen Eintrag in der Registrierungs Tabelle, um diesen Fehler zu beheben.<br/>                                                                                                                                                                                                                                                                                                                               |
| Die Komponente Component3 enthält nicht angekündigte Verknüpfungen. Der Schlüssel Pfad-Registrierungsschlüssel muss unter HKCU liegen.                                       | Die Spalte Attribute ist auf die Verwendung der Registrierung festgelegt, aber der Registrierungs Eintrag, auf den verwiesen wird, befindet sich nicht unter HKCU. Um diesen Fehler zu beheben, wechseln Sie entweder zu einem anderen Registrierungs Eintrag als KEYPATH für diese Komponente, oder ändern Sie den Stammwert des Registrierungs Eintrags entweder in-1 oder 1.<br/>                                                                                                                                                                                                                                                                             |
| Der KEYPATH-Registrierungs Eintrag für die Komponente Component4 ist nicht vorhanden.                                                                     | Der Registrierungs Eintrag, auf den in der KEYPATH-Spalte der Komponente verwiesen wird, befindet sich nicht in der Registrierungs Tabelle. Erstellen Sie einen Eintrag, um diesen Fehler zu beheben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Der Registrierungs Eintrag Reg5 wird als KEYPATH für die Komponente Component5 festgelegt, aber dieser Registrierungs Eintrag gehört nicht zu Component5.          | In der KEYPATH-Spalte der Komponente, die sich unter der HKCU-Struktur befindet, wird ein Registrierungs Eintrag erstellt, aber die Komponenten Spalte des Registrierungs Eintrags \_ verweist nicht auf dieselbe Komponente, die Sie als KEYPATH aufgelistet hat. Dies bedeutet, dass der Registrierungs Eintrag, der als KEYPATH der Komponente verwendet wird, nur dann erstellt wird, wenn eine andere Komponente installiert wurde. Um diesen Fehler zu beheben, ändern Sie den KEYPATH-Wert so, dass er auf einen Registrierungs Eintrag verweist, der zur Komponente gehört, oder ändern Sie den Registrierungs Eintrag so, dass er zur Komponente gehört, die ihn als KEYPATH verwendet.<br/>   |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | Attribute | KEYPATH |
|------------|------------|---------|
| Component1 | 0          | Datei1   |
| Component2 | 4          |         |
| Component3 | 4          | Reg3    |
| Component4 | 4          | Reg4    |
| Component5 | 4          | Reg5    |



 

[Registrierungs Tabelle](registry-table.md) (partiell)



| Registrierung | Root | Wert | Komponente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




