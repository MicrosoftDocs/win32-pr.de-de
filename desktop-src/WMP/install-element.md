---
title: Install-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das install-Element gibt Werte an, die von Windows Media Player verwendet werden, um einen Online Shop zu installieren.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Element Windows-Media Player installieren
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372257"
---
# <a name="install-element"></a>Install-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **install** -Element gibt Werte an, die von Windows Media Player verwendet werden, um einen Online Shop zu installieren.

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

<span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**Eulaurl** (erforderlich)
</dt> <dd>

Voll qualifizierte URL für eine Datei mit der Dateinamenerweiterung ". txt", die Windows Media Player verwendet, um einen Endbenutzer-Lizenzvertrag (EULA) anzuzeigen. Diese Datei muss im ANSI-Format codiert werden.

</dd> <dt>

<span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**Codeurl** (erforderlich)
</dt> <dd>

Voll qualifizierte URL für ein Paket mit der Dateinamenerweiterung ". cab", die zur Installation des Online Ladens verwendet wird. Das Paket und alle Code Module im Paket müssen signiert sein. Weitere Informationen zum Signieren von Code finden Sie unter Einführung in die [Code Signatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in der MSDN Library.

</dd> <dt>

<span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**Privacyinfourl** (erforderlich)
</dt> <dd>

Voll qualifizierte URL für eine Webseite, die Informationen zu Datenschutzbestimmungen für den Online Store enthält.

</dd> <dt>

<span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**Installapp** (erforderlich)
</dt> <dd>

Der Name der exe-oder INF-Datei, die ausgeführt werden soll. Diese Datei muss in der vom Attribut " **codeurl** " angegebenen CAB-Datei enthalten sein.

</dd> <dt>

<span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**Installdata** (optional)
</dt> <dd>

Befehlszeilen Zeichenfolge, die an die durch das **installapp** -Attribut angegebene Anwendung übermittelt wird. Dieses Attribut ist nur anwendbar, wenn der Wert für **installapp** eine ausführbare Datei angibt.

</dd> <dt>

<span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**Catalogurl** (erforderlich für Typ 1, wird für Typ 2 ignoriert)
</dt> <dd>

Voll qualifizierte URL für den kompilierten Katalog des Online Stores.

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Wenn eines der erforderlichen Attribute fehlt oder nicht verfügbar ist, versucht das Windows Media Player-Setup nicht, den Code des Online Store-Anbieters herunterzuladen und zu installieren. Setup konfiguriert die Offline Standardwerte entsprechend den Angaben im **serviceInfo** -Dokument. **ServiceInfo** kann verwendet werden, wenn keine Internet Verbindung besteht, indem der Standardanbieter Name und die **serviceInfo** -Informationen als Befehlszeilenparameter übergeben werden. Ausführliche Informationen zu Befehlszeilenoptionen finden Sie unter [Neuverteilen von Windows Media Player-Software](redistributing-windows-media-player-software.md) .

> [!Note]  
> Die Verwendung dieses Elements erfordert, dass Sie eine Verteilungs Vereinbarung mit Microsoft signieren. Weitere Informationen erhalten Sie von Ihrem Unternehmens Beauftragten.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

