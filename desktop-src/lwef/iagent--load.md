---
title: Iagent-Auslastung
description: Iagent-Auslastung
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948719"
---
# <a name="iagentload"></a>Iagent:: Load

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

Lädt ein Zeichen in die [**Zeichen**](./iagent.md) Auflistung.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vloadkey*
</dt> <dd>

Ein Variant-Datentyp, bei dem es sich um einen der folgenden Typen handeln muss:



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| *Datei Angabe* | Der lokale Datei Speicherort der Definitionsdatei des angegebenen Zeichens. |
| *URL*      | Die http-Adresse für die Definitionsdatei des Zeichens.                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwcharid*
</dt> <dd>

Adresse einer Variablen, die die ID des Zeichens empfängt.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, die die [**Auslastungs**](load-method.md) Anforderungs-ID empfängt.

</dd> </dl>

Sie können Zeichen aus dem Unterverzeichnis Microsoft Agent laden, indem Sie einen relativen Pfad angeben (einer, der keinen Doppelpunkt oder vorangestellenden Schrägstrich enthält). Dadurch wird der Pfad mit dem Zeichen Verzeichnis des Agents (befindet sich im lokalisierten% Windows% \\ MSAgent-Verzeichnis) als Präfix versehen. Sie können auch eine relative Adresse verwenden, um Ihr eigenes Verzeichnis im chars-Verzeichnis des Agents anzugeben.

Es ist nicht möglich, dasselbe Zeichen (ein Zeichen mit derselben GUID) mehrmals aus einer einzelnen Verbindung zu laden. Ebenso können Sie das Standard Zeichen und andere Zeichen nicht gleichzeitig von einer einzelnen Verbindung laden, da das Standard Zeichen mit dem anderen Zeichen identisch sein könnte. Sie können jedoch eine weitere Verbindung (mit cokreatanstance) erstellen und das gleiche Zeichen laden.

Der Microsoft Agent-Datenanbieter unterstützt das Laden von Zeichendaten, die als einzelne strukturierte Datei () gespeichert sind. ACS) mit Zeichendaten und Animationsdaten oder als separate Zeichendaten (. ACF) und Animation (. ACA-Dateien. Verwenden Sie im Allgemeinen die strukturierte Struktur. Die ACS-Datei zum Laden eines Zeichens, das auf einem lokalen Laufwerk oder Netzwerk gespeichert ist und auf das ein herkömmliches Datei Protokoll (z. b. UNC-Pfadnamen) zugegriffen wird. Verwenden Sie die separate. ACF und. ACA-Dateien, wenn Sie die Animationsdateien einzeln von einer Remote Site laden möchten, auf die über das HTTP-Protokoll zugegriffen wird.

Damit. ACS-Dateien, die die [**Load**](load-method.md) -Methode verwenden, bieten Zugriff auf die Animationen eines Zeichens. nach dem Laden können Sie das Zeichen mit der [**Play**](play-method.md) -Methode animieren. Damit. ACF-Dateien verwenden Sie auch die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um Animationsdaten zu laden. Die **Load** -Methode unterstützt nicht das herunterladen. ACS-Dateien von einer HTTP-Site.

Beim Laden eines Zeichens wird das Zeichen nicht automatisch angezeigt. Verwenden Sie zuerst die [**Show**](show-method.md) -Methode, um das Zeichen sichtbar zu machen.

 

 