---
title: Co-Branding Onlineshops
description: Co-Branding Onlineshops
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player Onlineshops, Co-Branding
- Onlineshops, Co-Branding
- Geben Sie 1 Onlineshops ein, Co-Branding
- Geben Sie 2 Onlineshops ein, Co-Branding
- Co-Branding von Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3ca69c377a7aedeb71f05008d707fab955f02bf0e02d7b0ca35861105aade1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342131"
---
# <a name="co-branding-online-stores"></a>Co-Branding Onlineshops

OEMs für Personalcomputer, die keinen Musikspeicher betreiben, können eine Co-Marke mit Onlineshopanbietern verwenden. Windows Media Player Setup unterstützt den ServiceExtra-Befehlszeilenparameter, um Hardware-OEMs das Festlegen eines benutzerdefinierten Attributs zu ermöglichen, mit dem der Onlineshop ermitteln kann, welcher OEM den ursprünglichen Onlineshop installiert hat.

Wenn beispielsweise ein Computerhersteller namens Fabrikam den ersten Onlineshop auf den Proseware-Musikspeicher festlegen möchte, kann er die folgende Befehlszeile verwenden, um Windows Media Player 10 zu installieren:


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



Wenn Windows Media Player auf diese Weise installiert wird, fügt der Player die ServiceExtra-Zeichenfolge jedes Mal an, wenn der Proseware-Dienst geöffnet wird. Das folgende Beispiel zeigt die URL, die Windows Media Player an den Proseware-Dienst senden würde, um das ServiceInfo-Dokument abzurufen:


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



Der Proseware-Onlineshop kann dann die Abfragezeichenfolge verwenden, um zu bestimmen, welcher OEM Windows Media Player installiert wurde, und ein dynamisch generiertes ServiceInfo-Dokument zurückgeben, das auf die Co-Brandingversion des Onlineshops verweist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und Typ 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Einrichten von Befehlszeilenparametern für Onlineshops**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




