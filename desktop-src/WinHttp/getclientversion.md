---
description: Ruft die Version der WPAD-Verarbeitungs-Engine ab.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: GetClientVersion-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866231"
---
# <a name="getclientversion-function"></a>GetClientVersion-Funktion

Ruft die Version der WPAD-Verarbeitungs-Engine ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*Ipaddresslist* 
</dt> <dd>

Eine durch Semikolons getrennte Zeichenfolge, die IP-Adressen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Liste von durch Trennzeichen getrennten, durch Semikola getrennten IP-Adressen oder eine leere Zeichenfolge, wenn die IP-Adressliste nicht sortiert werden kann.

## <a name="remarks"></a>Bemerkungen

Diese Funktion gibt derzeit Version 1,0 zurück.

Microsoft hat diese Funktion hinzugefügt, damit IT-Administratoren ihre WPAD-Skripts aktualisieren können, um unterschiedliche Versionen der WPAD-Verarbeitungs-Engine zu verwenden, ohne dass die vorhandene Bereitstellung unterbrochen wird. Wenn Microsoft z. b. der 2,0-Version der WPAD-Engine eine Funktion hinzugefügt hat, können Administratoren die Version überprüfen, bevor Sie versuchen, diese Funktion aufzurufen. Dadurch kann das Skript mit dem Client ausgeführt werden, auf dem die Versionen 1,0 und 2,0 der WPAD-Engine ausgeführt werden.

## <a name="examples"></a>Beispiele

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IPv6-abhängige proxyhilfsobjekts-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



