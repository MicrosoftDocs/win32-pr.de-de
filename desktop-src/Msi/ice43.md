---
description: ICE43 überprüft, ob Verknüpfungen, die nicht auf ein Feature als Ziel verweisen (nicht angekündigte Verknüpfungen), sich in Komponenten befinden, die einen HKCU-Registrierungseintrag als Schlüsselpfad haben.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69af661b22d851b50a74bdffb9534b1e269dde4e428440882ee2d52813a68c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635206"
---
# <a name="ice43"></a>ICE43

ICE43 überprüft, ob Verknüpfungen, die nicht auf ein Feature als Ziel verweisen (nicht angekündigte Verknüpfungen), sich in Komponenten befinden, die einen HKCU-Registrierungseintrag als Schlüsselpfad haben.

## <a name="result"></a>Ergebnis

ICE43 gibt eine Fehlermeldung aus, wenn sich eine nicht angekündigte Verknüpfung in einer Komponente befindet, die nicht über einen HKCU-Registrierungseintrag als Schlüsselpfad verfügt.

## <a name="example"></a>Beispiel

ICE43 würde die folgenden Fehler für das gezeigte Beispiel melden.



| ICE43-Fehler                                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Komponente Komponente1 verfügt über nicht angekündigte Verknüpfungen. Er muss einen Registrierungsschlüssel unter HKCU als KeyPath und nicht als Datei verwenden.                    | Die Spalte attributes von Component1 ist 0, was bedeutet, dass die Komponente eine Datei als KeyPath verwendet. Dies bewirkt, dass nicht angekündigte Verknüpfungen in dieser Komponente nur für den ersten Benutzer auf dem Computer installiert werden. Benutzern, die die Komponente später installieren, werden die Verknüpfungen nicht angezeigt, da die Komponente für das Installationsprogramm als bereits auf dem Computer vorhanden angezeigt wird. Um diesen Fehler zu beheben, legen Sie das RegistryKeyPath-Bit der Attribute so fest, dass die Komponente in einen Registrierungseintrag wechselt, und ändern Sie dann den KeyPath-Wert in einen gültigen Eintrag in der Registrierungstabelle.<br/> |
| Komponente 2 verfügt über nicht angekündigte Verknüpfungen. Er muss einen Registrierungsschlüssel unter HKCU als KeyPath verwenden. Der KeyPath ist derzeit NULL. | Die Attributes -Spalte ist für die Verwendung der Registrierung festgelegt, aber der KeyPath ist NULL. KeyPath muss auf einen Eintrag in der Registrierungstabelle verweisen. Um diesen Fehler zu beheben, ändern Sie den KeyPath-Wert in einen gültigen Eintrag in der Tabelle Registrierung.<br/>                                                                                                                                                                                                                                                                                                                               |
| Komponente 3 verfügt über nicht angekündigte Verknüpfungen. Der KeyPath-Registrierungsschlüssel muss unter HKCU fallen.                                       | Die Spalte Attribute ist für die Verwendung der Registrierung festgelegt, aber der Registrierungseintrag, auf den verwiesen wird, befindet sich nicht unter HKCU. Um diesen Fehler zu beheben, wechseln Sie entweder zu einem anderen Registrierungseintrag als KeyPath für diese Komponente, oder ändern Sie den Root-Wert des Registrierungseintrags in -1 oder 1.<br/>                                                                                                                                                                                                                                                                             |
| Der KeyPath-Registrierungseintrag für Komponente Component4 ist nicht vorhanden.                                                                     | Der Registrierungseintrag, auf den in der KeyPath-Spalte der Komponente verwiesen wird, befindet sich nicht in der Registrierungstabelle. Um diesen Fehler zu beheben, erstellen Sie einen Eintrag.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Der Registrierungseintrag Reg5 wird als KeyPath für Komponente Component5 festgelegt, aber dieser Registrierungseintrag gehört nicht zu Component5.          | Es gibt einen Registrierungseintrag, auf den in der KeyPath -Spalte der Komponente verwiesen wird, der sich unter der HKCU-Struktur befindet, aber die Spalte Component des Registrierungseintrags verweist nicht auf dieselbe Komponente, die sie als KeyPath aufgelistet \_ hat. Dies bedeutet, dass der Registrierungseintrag, der als KeyPath der Komponente verwendet wird, nur erstellt wird, wenn eine andere Komponente installiert wurde. Um diesen Fehler zu beheben, ändern Sie den KeyPath-Wert, um auf einen Registrierungseintrag zu verweisen, der zur Komponente gehört, oder ändern Sie den Registrierungseintrag so, dass er zur Komponente gehört, indem Sie ihn als KeyPath verwenden.<br/>   |



 

[Komponententabelle](component-table.md) (partiell)



| Komponente  | Attribute | KeyPath |
|------------|------------|---------|
| Komponente1 | 0          | Datei1   |
| Component2 | 4          |         |
| Component3 | 4          | Reg3    |
| Component4 | 4          | Reg4    |
| Komponente5 | 4          | Reg5    |



 

[Registrierungstabelle](registry-table.md) (partiell)



| Registrierung | Root | Wert | Komponente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




