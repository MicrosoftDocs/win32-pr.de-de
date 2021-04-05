---
title: Iagentcharakteriex gezrmodeid
description: Iagentcharakteriex gezrmodeid
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723813"
---
# <a name="iagentcharacterexgetsrmodeid"></a>Iagentcharakteriex:: gezrmodeid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

Ruft die Mode-ID des sprach Erkennungs Moduls für das Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszmodeid*
</dt> <dd>

Adresse eines BSTR, der die Modus-ID-Einstellung der sprach Erkennungs-Engine für das Zeichen empfängt.

</dd> </dl>

Diese Einstellung gibt den Engine-Satz für die Spracheingabe eines Zeichens zurück. Die Mode-ID für eine Spracherkennungs-Engine ist eine Zeichen folgen Darstellung der GUID (mit geschweiften Klammern und Bindestrichen formatiert), indem der Sprachanbieter die Engine eindeutig identifiziert. Weitere Informationen finden Sie in der [Microsoft Speech SDK-Dokumentation](https://msdn.microsoft.com/library/ee705648.aspx).

Wenn Sie keine sprach Erkennungs-Engine-Modus-ID für das Zeichen festlegen, gibt der Server eine Engine zurück, die der Spracheinstellung des Zeichens (über die Microsoft Speech API-Schnittstellen) entspricht. Wenn keine übereinstimmende sprach Erkennungs-Engine für das Zeichen verfügbar ist, gibt der Server eine NULL-Zeichenfolge (leere Zeichenfolge) zurück.

Wenn die Spracheingabe aktiviert ist (im Fenster Erweiterte Zeichen Optionen), wird durch das Abfragen oder Festlegen dieser Eigenschaft die zugeordnete Engine geladen (falls Sie nicht bereits geladen wurde), und die Sprachdienste werden gestartet. Das heißt, der lauschende Schlüssel ist verfügbar, und der Abhör Tipp kann angezeigt werden. (Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server keine Sprachdienste und gibt eine NULL-Zeichenfolge (leere Zeichenfolge) zurück.

Diese Funktion gibt nur die Einstellung für die Verwendung des Zeichens durch die Client Anwendung zurück. die Einstellung entspricht nicht anderen Clients des Zeichens oder anderen Zeichen ihrer Client Anwendung.

Diese Funktion schlägt fehl, wenn [**iagentspeechinputproperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md) **false** zurückgibt.

Die Sprach-Engine-Anforderungen von Microsoft Agent basieren auf der Microsoft Speech-API. Module, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können installiert und mit dem-Agent verwendet werden

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex::-rzrmodeid**](iagentcharacterex--setsrmodeid.md)


 

 




