---
title: Co-Branding von Online Stores
description: Co-Branding von Online Stores
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player Online Stores, Co-Branding
- Online Stores, Co-Branding
- Typ 1 Online Stores, Co-Branding
- Typ 2 Online Stores, Co-Branding
- Co-Branding von Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339201"
---
# <a name="co-branding-online-stores"></a>Co-Branding von Online Stores

Persönliche Computer OEMs, die keinen Musikspeicher betreiben, können mit Online Store-Anbietern mitmarken. Das Windows Media Player-Setup unterstützt den Befehlszeilenparameter "serviceextra", damit Hardware OEMs ein benutzerdefiniertes Attribut festlegen können, das der Online Shop verwenden kann, um zu ermitteln, welcher OEM den ursprünglichen Online Store installiert hat

Wenn z. b. ein Computerhersteller mit dem Namen Fabrikam den anfänglichen Online Store auf den Proseware Music Store festlegen möchte, kann die folgende Befehlszeile zum Installieren von Windows Media Player 10 verwendet werden:


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



Wenn Windows Media Player auf diese Weise installiert wird, fügt der Player die serviceextra-Zeichenfolge jedes Mal an, wenn der Proseware-Dienst geöffnet wird. Das folgende Beispiel zeigt die URL, die von Windows Media Player an den Proseware-Dienst gesendet wird, um das serviceInfo-Dokument abzurufen:


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



Der Proseware Online Store kann dann mithilfe der Abfrage Zeichenfolge ermitteln, welche OEM-Media Player installierte Windows-und ein dynamisch generiertes serviceInfo-Dokument zurückgeben, das auf die Version des Online Stores mit dem Marken Format verweist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Einrichten von Befehlszeilen Parametern für Online Stores**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




