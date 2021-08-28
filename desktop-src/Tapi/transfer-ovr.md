---
description: Mit dem Übertragungsvorgang kann eine Anwendung eine derzeit verbundene Kommunikationssitzung an eine andere Adresse senden.
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: Übertragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bb527ad8e0a26ba5e4da341eb15509e8af05e7950d82de92be839e70370c79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514540"
---
# <a name="transfer"></a>Übertragen

Mit dem Übertragungsvorgang kann eine Anwendung eine derzeit verbundene Kommunikationssitzung an eine andere Adresse senden.

TAPI bietet zwei Mechanismen zum Übertragen einer aktuellen Sitzung an eine andere Adresse. *Die blinde* Übertragung ermöglicht es, eine vorhandene Sitzung in einer Phase an eine angegebene Zieladresse zu übertragen. *Die Übertragung der* Beratung erfordert das Vorhandensein einer Beratungssitzung zusätzlich zur aktuellen Sitzung, die für die Übertragung eingerichtet werden muss, und dann den Abschluss der Übertragung. Die Wahl zwischen diesen beiden Typen basiert häufig auf Dienstanbieterfunktionen, da einige Dienstanbieter die blinde Übertragung nicht unterstützen. In einigen Fällen können Anwendungsanforderungen dazu führen, dass die Übertragung der C übertragenen Daten zur bevorzugten Methode wird, auch wenn eine blinde Übertragung möglich ist.

Der blinde Übertragungsvorgang ist im Grunde derselbe unter TAPI 2 und TAPI 3, aber die C task-Übertragung folgt etwas anderen Mustern.

**TAPI 2.x:** C übertragen beginnt mit dem Aufrufen von [**lineSetupTransfer,**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)wodurch der vorhandene Anruf in die Beratung einbehalten wird, und identifiziert diesen Aufruf als Ziel für die nächste Übertragungsvervollständigungsanforderung. Die **lineSetupTransfer-Funktion** ordnet auch einen Beratungsanruf zu, der verwendet werden kann, um den Beratungsanruf mit der Partei zu erstellen, an die der Anruf übertragen wird. Die Anwendung kann die Erweiterung der Ziel-Partei beim Beratungsanruf wählen (mit [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)), oder sie kann den Beratungsanruf ablegen und seine Position wieder auffinden und stattdessen einen vorhandenen gehaltenen Anruf aktivieren (mithilfe von [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)), wenn er vom Schalter unterstützt wird. Während sich der erste Anruf in der Beratungsphase befindet und der Telefonanruf aktiv ist, kann die Anwendung mithilfe von [**lineSwapHold**](/windows/win32/api/tapi/nf-tapi-lineswaphold)zwischen diesen Aufrufen umschalten.

**TAPI 2.x:** Anwendungen schließen die Übertragung mit [**lineCompleteTransfer ab.**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) Beide Aufrufe werden in den *Leerlaufzustand* zurückverwendet.

Anwendungen können das Feature "1-Schritt-Übertragung" vieler PBX-Dateien verwenden (ein einzelner Tastendruck, um eine gemeinsame Übertragung zu erstellen), indem der *lpCallParams-Parameter* auf das **LINECALLPARAMFLAGS \_ ONESTEPTRANSFER-Mitglied** der [ \_ LINECALLPARAMFLAGS-Konstanten](./linecallparamflags--constants.md) beim Aufrufen [**von lineSetupTransfer festlegen.**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)

**TAPI 3.x:** C übertragen beginnt mit der [**Verwendung von ITAddress::CreateCall,**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) um einen Beratungsanruf an die neue Zieladresse zu erstellen. [**ITBasicCallControl::Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) wird dann für das ursprüngliche Aufrufobjekt aufgerufen, indem ein Zeiger auf das neue Beratungsaufrufobjekt als Parameter verwendet wird. Der [**Aufruf von ITBasicCallControl::Finish für**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) das Beratungsaufrufobjekt schließt dann die Übertragung ab.

Die Anwendung muss Sitzungsressourcen nach dem erfolgreichen Abschluss eines Übertragungsvorgang frei geben.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2.x:** Siehe [**lineBlindTransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer).

**TAPI 3.x:** Weitere Informationen finden Sie unter [**ITBasicCallControl::BlindTransfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer), [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), [**ITBasicCallControl::Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer), [**ITBasicCallControl::Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish).

 

 
