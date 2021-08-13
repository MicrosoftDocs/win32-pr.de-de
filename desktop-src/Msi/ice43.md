---
description: ICE43 überprüft, ob Verknüpfungen, die nicht auf ein Feature verweisen, als Ziel (nicht angekündigte Verknüpfungen) in Komponenten enthalten sind, die über einen HKCU-Registrierungseintrag als Schlüsselpfad verfügen.
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

ICE43 überprüft, ob Verknüpfungen, die nicht auf ein Feature verweisen, als Ziel (nicht angekündigte Verknüpfungen) in Komponenten enthalten sind, die über einen HKCU-Registrierungseintrag als Schlüsselpfad verfügen.

## <a name="result"></a>Ergebnis

ICE43 sendet eine Fehlermeldung, wenn sich eine nicht angekündigte Verknüpfung in einer Komponente befindet, die keinen HKCU-Registrierungseintrag als Schlüsselpfad aufweist.

## <a name="example"></a>Beispiel

ICE43 meldet die folgenden Fehler für das gezeigte Beispiel.



| ICE43-Fehler                                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Komponente Komponente1 verfügt über nicht angekündigte Verknüpfungen. Es muss einen Registrierungsschlüssel unter HKCU als KeyPath und keine Datei verwenden.                    | Die Attributspalte von Component1 ist 0, was bedeutet, dass die Komponente eine Datei als KeyPath verwendet. Dies führt dazu, dass nicht angekündigte Verknüpfungen in dieser Komponente nur für den ersten Benutzer auf dem Computer installiert werden. Benutzern, die die Komponente später installieren, werden die Verknüpfungen nicht angezeigt, da die Komponente dem Installationsprogramm als bereits auf dem Computer vorhanden angezeigt wird. Um diesen Fehler zu beheben, legen Sie das RegistryKeyPath-Bit der Attribute fest, um die Komponente in einen Registrierungseintrag zu ändern, und ändern Sie dann den KeyPath-Wert in einen gültigen Eintrag in der Tabelle Registry.<br/> |
| Komponente Komponente 2 verfügt über nicht angekündigte Verknüpfungen. Es muss einen Registrierungsschlüssel unter HKCU als KeyPath verwenden. KeyPath ist derzeit NULL. | Die Spalte Attribute ist auf die Verwendung der Registrierung festgelegt, aber KeyPath ist NULL. KeyPath muss auf einen Eintrag in der Registrierungstabelle verweisen. Um diesen Fehler zu beheben, ändern Sie den KeyPath-Wert in einen gültigen Eintrag in der Registrierungstabelle.<br/>                                                                                                                                                                                                                                                                                                                               |
| Komponente Komponente 3 verfügt über nicht angekündigte Verknüpfungen. Sein KeyPath-Registrierungsschlüssel muss unter HKCU fallen.                                       | Die Spalte Attribute ist auf die Verwendung der Registrierung festgelegt, aber der Registrierungseintrag, auf den verwiesen wird, befindet sich nicht unter HKCU. Um diesen Fehler zu beheben, wechseln Sie entweder zu einem anderen Registrierungseintrag als KeyPath für diese Komponente, oder ändern Sie den Root-Wert des Registrierungseintrags in -1 oder 1.<br/>                                                                                                                                                                                                                                                                             |
| Der KeyPath-Registrierungseintrag für komponente Component4 ist nicht vorhanden.                                                                     | Der Registrierungseintrag, auf den in der KeyPath-Spalte der Komponente verwiesen wird, befindet sich nicht in der Registrierungstabelle. Erstellen Sie einen Eintrag, um diesen Fehler zu beheben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Der Registrierungseintrag Reg5 wird als KeyPath für die Komponente Component5 festgelegt, aber dieser Registrierungseintrag gehört nicht zu Component5.          | Es gibt einen Registrierungseintrag, auf den in der KeyPath-Spalte der Komponente verwiesen wird, der sich unter der HKCU-Struktur befindet, aber die Spalte Komponente des Registrierungseintrags \_ verweist nicht auf dieselbe Komponente, die sie als KeyPathauflistet hat. Dies bedeutet, dass der Registrierungseintrag, der als KeyPath der Komponente verwendet wird, nur erstellt wird, wenn eine andere Komponente installiert wurde. Um diesen Fehler zu beheben, ändern Sie den KeyPath-Wert so, dass er auf einen Registrierungseintrag verweist, der zur Komponente gehört, oder ändern Sie den Registrierungseintrag so, dass er zur Komponente gehört, indem Sie ihn als KeyPath verwenden.<br/>   |



 

[Komponententabelle](component-table.md) (teilweise)



| Komponente  | Attribute | KeyPath |
|------------|------------|---------|
| Komponente1 | 0          | Datei1   |
| Component2 | 4          |         |
| Component3 | 4          | Reg3    |
| Komponente4 | 4          | Reg4    |
| Komponente5 | 4          | Reg5    |



 

[Registrierungstabelle](registry-table.md) (partiell)



| Registrierung | Root | Wert | Komponente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Komponente4  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




