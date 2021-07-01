---
title: IAgent Load
description: IAgent Load
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce2835d60f3edce6f45d181927437ba6e58b18
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120933"
---
# <a name="iagentload"></a>IAgent::Load

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

Lädt ein Zeichen in die [**Characters-Auflistung.**](./iagent.md)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*
</dt> <dd>

Ein variant-Datentyp, der einen der folgenden Sein muss:



| Wert           | Beschreibung                                                                      |
|------------|-----------------------------------------------------------------------|
| *Dateinamen* | Der lokale Dateispeicherort der Definitionsdatei des angegebenen Zeichens. |
| *URL*      | Die HTTP-Adresse für die Definitionsdatei des Zeichens.                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*
</dt> <dd>

Adresse einer Variablen, die die ID des Zeichens empfängt.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die die [**Load-Anforderungs-ID**](load-method.md) empfängt.

</dd> </dl>

Sie können Zeichen aus dem Microsoft-Agent-Unterverzeichnis laden, indem Sie einen relativen Pfad angeben (einen Pfad, der keinen Doppelpunkt oder führenden Schrägstrich enthält). Dadurch wird dem Pfad das Zeichenverzeichnis des -Agents vorangestellt (im lokalisierten Verzeichnis %windows% \\ msagent). Sie können auch eine relative Adresse verwenden, um Ihr eigenes Verzeichnis im Chars-Verzeichnis des Agents anzugeben.

Sie können das gleiche Zeichen (ein Zeichen mit derselben GUID) nicht mehr als einmal aus einer einzelnen Verbindung laden. Ebenso können Sie das Standardzeichen und andere Zeichen nicht gleichzeitig aus einer einzelnen Verbindung laden, da das Standardzeichen mit dem anderen Zeichen identisch sein kann. Sie können jedoch eine weitere Verbindung (mit CoCreateInstance) erstellen und das gleiche Zeichen laden.

Der Datenanbieter des Microsoft-Agents unterstützt das Laden von Zeichendaten, die als einzelne strukturierte Datei gespeichert sind (. ACS) mit Zeichendaten und Animationsdaten zusammen oder als separate Zeichendaten (. ACF) und Animation (. ACA)-Dateien. Verwenden Sie im Allgemeinen die einzelne strukturierte . ACS-Datei zum Laden eines Zeichens, das auf einem lokalen Laufwerk oder Netzwerk gespeichert ist und auf das mithilfe eines herkömmlichen Dateiprotokolls (z. B. UNC-Pfadnamen) zugegriffen wird. Verwenden Sie die separate . ACF und . ACA-Dateien, wenn Sie die Animationsdateien einzeln von einem Remotestandort laden möchten, auf den über das HTTP-Protokoll zugegriffen wird.

Für. ACS-Dateien, die die [**Load-Methode**](load-method.md) verwenden, bieten Zugriff auf die Animationen eines Zeichens. Nach dem Laden können Sie die [**Play-Methode**](play-method.md) verwenden, um das Zeichen zu animieren. Für. ACF-Dateien verwenden Sie auch die [**Prepare-Methode,**](/windows/desktop/lwef/iagentcharacter--prepare) um Animationsdaten zu laden. Das Herunterladen von wird von der **Load-Methode** nicht unterstützt. ACS-Dateien von einer HTTP-Website.

Beim Laden eines Zeichens wird das Zeichen nicht automatisch angezeigt. Verwenden [](show-method.md) Sie zuerst die Show-Methode, um das Zeichen sichtbar zu machen.

 

 