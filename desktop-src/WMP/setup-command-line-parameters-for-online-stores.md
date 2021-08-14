---
title: Einrichten von Befehlszeilenparametern für Onlineshops
description: Einrichten von Befehlszeilenparametern für Onlineshops
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player Onlineshops, Einrichten von Befehlszeilenparametern
- Onlineshops, Befehlszeilenparameter einrichten
- Geben Sie 1 Onlineshops ein, und richten Sie Befehlszeilenparameter ein.
- Geben Sie 2 Onlineshops ein, und richten Sie Befehlszeilenparameter ein.
- Einrichten von Befehlszeilenparametern
- Windows Media Player Onlineshops, Befehlszeilenparameter
- Onlineshops, Befehlszeilenparameter
- Geben Sie 1 Onlineshops ein, Befehlszeilenparameter
- Geben Sie 2 Onlineshops ein, Befehlszeilenparameter.
- Befehlszeilenparameter
- Windows Media Player Onlineshops, Parameter
- Onlineshops, Parameter
- Geben Sie 1 Onlineshops, Parameter ein.
- Geben Sie 2 Onlineshops, Parameter ein.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77df581b2be4b2539772065e1aabef281a4c6c931ca115a4f6331063cf2414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569301"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>Einrichten von Befehlszeilenparametern für Onlineshops

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Wenn Sie Windows Media Player 10 oder Windows Media Player 11 auf Windows XP installieren, können Sie Befehlszeilenparameter anfügen, um den ersten Onlineshop anzugeben, der dem Benutzer angezeigt wird.

Syntax


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



Parameter

DefaultService (erforderlich)

Der Schlüsselname für den Onlineshop. Dieser Wert muss mit dem Schlüsselnamen im **Key-Attribut** des **ServiceInfo-Elements** des ServiceInfo-Dokuments übereinstimmen.

ServiceInfo (erforderlich)

Der vollqualifizierte Pfad zu einem ServiceInfo-Dokument, das auf dem Computer des Benutzers installiert ist.

ServiceExtra (optional)

Eine Abfragezeichenfolge Windows Media Player 10 wird an die URL für das ServiceInfo-Dokument angefügt, wenn das Dokument online abgerufen wird.

## <a name="remarks"></a>Hinweise

Ausführliche Informationen zum Verteilen Windows Media Player Software mit Ihrer Anwendung finden Sie unter [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).

Wenn der Computer des Benutzers nicht mit dem Internet verbunden ist, werden die im lokalen ServiceInfo-Dokument enthaltenen Informationen verwendet, um Windows Media Player für den ersten aktiven Dienst zu konfigurieren.

Bei Befehlszeilenparametern wird die Groß-/Kleinschreibung beachtet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Co-Branding von Onlineshops**](co-branding-online-stores.md)
</dt> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und Typ 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Install-Element**](install-element.md)
</dt> <dt>

[**Festlegen des Store "Initial Online"**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




