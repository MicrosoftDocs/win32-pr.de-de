---
title: Install-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Das Install-Element gibt Werte an, die von Windows Media Player zum Installieren eines Onlineshops verwendet werden.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Install-Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05a946cbab6a6334faa7483c0f3201a98ff0abe32dca32fe1f4f7eed5d0a2408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996520"
---
# <a name="install-element"></a>Install-Element

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **Install-Element** gibt Werte an, die von Windows Media Player zum Installieren eines Onlineshops verwendet werden.

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (erforderlich)
</dt> <dd>

Vollqualifizierte URL für eine Datei mit .txt Dateierweiterung, die Windows Media Player zum Anzeigen eines Endbenutzer-Lizenzvertrags (EULA) verwendet. Diese Datei muss im ANSI-Format codiert sein.

</dd> <dt>

<span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (erforderlich)
</dt> <dd>

Vollqualifizierte URL für ein Paket mit .cab Dateierweiterung, die zum Installieren des Onlineshops verwendet wird. Das Paket und alle Codemodule im Paket müssen signiert sein. Informationen zum Signieren von Code finden Sie [unter Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in der MSDN Library.

</dd> <dt>

<span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (erforderlich)
</dt> <dd>

Vollqualifizierte URL für eine Webseite, die Datenschutzrichtlinieninformationen für den Onlineshop enthält.

</dd> <dt>

<span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (erforderlich)
</dt> <dd>

Der Name der exe- oder INF-Datei, die ausgeführt werden soll. Diese Datei muss in der CAB-Datei enthalten sein, die durch das **CodeURL-Attribut angegeben** wird.

</dd> <dt>

<span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (optional)
</dt> <dd>

Befehlszeilenzeichenfolge, die an die durch das **InstallApp-Attribut** angegebene Anwendung übergeben wird. Dieses Attribut ist nur anwendbar, wenn der Wert für **InstallApp** eine ausführbare Datei angibt.

</dd> <dt>

<span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (für Typ 1 erforderlich, für Typ 2 ignoriert)
</dt> <dd>

Vollqualifizierte URL für den kompilierten Katalog des Onlineshops.

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Wenn eines der erforderlichen Attribute fehlt oder nicht verfügbar ist, versucht Windows Media Player Setup nicht, den Code des Onlineshopanbieters herunterzuladen und zu installieren. Setup konfiguriert die Offline-Standardwerte wie im **ServiceInfo-Dokument** angegeben. **ServiceInfo** kann verwendet werden, wenn keine Internetverbindung besteht, indem der Standardanbietername und die **ServiceInfo-Informationen** als Befehlszeilenparameter übergeben werden. Weitere [Informationen zu Befehlszeilenoptionen finden Sie unter Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md) ( Redistributing Windows Media Player Software ).

> [!Note]  
> Die Verwendung dieses Elements erfordert, dass Sie einen Weiterverteilungsvertrag mit Microsoft unterzeichnen. Wenden Sie sich an Ihren Geschäftsmitarbeiter, um Weitere Informationen zu erhalten.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

