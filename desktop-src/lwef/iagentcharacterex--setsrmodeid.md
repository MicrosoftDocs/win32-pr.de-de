---
title: Iagentcharakteriex--rzrmodeid
description: Iagentcharakteriex--rzrmodeid
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104472260"
---
# <a name="iagentcharacterexsetsrmodeid"></a>Iagentcharakteriex::-rzrmodeid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

Legt die Mode-ID des sprach Erkennungs Moduls für das Zeichen fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

bszmodeid

Die Modus-ID-Einstellung der sprach Erkennungs-Engine für das Zeichen.

Mit dieser Einstellung wird die-Engine für die Spracheingabe eines Zeichens festgelegt. Die Mode-ID für eine Spracherkennungs-Engine ist die GUID, die vom Sprachanbieter definiert wird, der den Modus der Engine eindeutig identifiziert (mit geschweiften Klammern und Bindestrichen formatiert). Weitere Informationen finden Sie in der [Microsoft Speech SDK-Dokumentation](https://msdn.microsoft.com/library/ee705648.aspx).

Wenn Sie eine Mode-ID angeben, die nicht mit der Spracheinstellung des Zeichens identisch ist, tritt bei diesem Vorgang ein Fehler auf, wenn der Benutzer die Spracherkennung deaktiviert hat (auf dem Eigenschaften Blatt des Microsoft-Agents) oder die-Engine nicht installiert ist. Wenn Sie keine sprach Erkennungs-Engine-Modus-ID für das Zeichen festlegen, legt der Server einen fest, der mit der Spracheinstellung des Zeichens (über die Microsoft Speech API-Schnittstellen) übereinstimmt.

Wenn die Spracheingabe auf der Eigenschaften Seite des-Agents aktiviert ist (erweiterte Zeichen Optionen), wird durch das Festlegen dieser Eigenschaft die zugeordnete Engine geladen (sofern Sie nicht bereits geladen wurde) und Sprachdienste starten. Das heißt, der lauschende Schlüssel ist verfügbar, und der Abhör Tipp kann angezeigt werden. (Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server die Sprachdienste nicht.

Diese Eigenschaft gilt nur für den Client des Zeichens. die Einstellung entspricht nicht der Einstellung für andere Clients des Zeichens oder anderen Zeichen des Clients.

Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API. Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex:: gezrmodeid**](iagentcharacterex--getsrmodeid.md)


 

 




