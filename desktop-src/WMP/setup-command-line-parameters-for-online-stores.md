---
title: Einrichten von Befehlszeilen Parametern für Online Stores
description: Einrichten von Befehlszeilen Parametern für Online Stores
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player Online Stores, Setup-Befehlszeilenparameter
- Online Stores, Setup-Befehlszeilenparameter
- Typ 1 Online Stores, Setup Befehlszeilenparameter
- Typ 2 Online Stores, Setup Befehlszeilenparameter
- Setup-Befehlszeilenparameter
- Windows Media Player Online Stores, Befehlszeilenparameter
- Online Stores, Befehlszeilenparameter
- Typ 1 Online Stores, Befehlszeilenparameter
- Typ 2 Online Stores, Befehlszeilenparameter
- Befehlszeilenparameter
- Windows Media Player Online Stores, Parameter
- Online Stores, Parameter
- Typ 1 Online Stores, Parameter
- Typ 2 Online Stores, Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036895"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>Einrichten von Befehlszeilen Parametern für Online Stores

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Bei der Installation von Windows Media Player 10 oder Windows Media Player 11 unter Windows XP können Sie Befehlszeilenparameter anfügen, um den ersten Onlinespeicher anzugeben, der dem Benutzer angezeigt wird.

Syntax


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



Parameter

Defaultservice (erforderlich)

Der Schlüssel Name für den Online Shop. Dieser Wert muss mit dem Schlüsselnamen im **Key** -Attribut des **serviceInfo** -Elements des serviceInfo-Dokuments übereinstimmen.

Serviceingefo (erforderlich)

Der voll qualifizierte Pfad zu einem serviceInfo-Dokument, das auf dem Computer des Benutzers installiert ist.

Serviceextra (optional)

Eine Abfrage Zeichenfolge, die von Windows Media Player 10 an die URL des serviceingefo-Dokuments angehängt wird, wenn das Dokument online abgerufen wird.

## <a name="remarks"></a>Bemerkungen

Ausführliche Informationen zur Neuverteilung von Windows Media Player-Software mit Ihrer Anwendung finden Sie unter [Verteilen von Windows Media Player Software](redistributing-windows-media-player-software.md).

Wenn der Computer des Benutzers nicht mit dem Internet verbunden ist, werden die im lokalen serviceInfo-Dokument enthaltenen Informationen verwendet, um Windows-Media Player für den ersten aktiven Dienst zu konfigurieren.

Bei Befehlszeilen Parametern wird Groß-/Kleinschreibung beachtet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Co-Branding von Online Stores**](co-branding-online-stores.md)
</dt> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Install-Element**](install-element.md)
</dt> <dt>

[**Festlegen des ersten Online Stores**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




