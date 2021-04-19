---
description: Die Locale-Eigenschaft des "errbemubjectpath"-Objekts enthält das Gebiets Schema des Objekt Pfads.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Errbemubjectpath. Locale-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358582"
---
# <a name="swbemobjectpathlocale-property"></a>Errbemubjectpath. Locale (Eigenschaft)

Die **locale** -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts enthält das Gebiets Schema des Objekt Pfads.

Wenn die Eigenschaft " **errbemubjectpath. locale** " Teil eines eigenständigen " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts ist, ist Sie Lese-/Schreibzugriff und kann verwendet werden, um die Gebiets Schema Komponente des Monikers festzulegen.

Wenn auf die Eigenschaft " **errbemubjectpath. locale** " als Teil einer " [**errbemubject. \_ path**](swbemobject-path-.md) "-Eigenschaft zugegriffen wird, ist sie schreibgeschützt und meldet den Wert des Gebiets Schemas, das bei der Bindung an den Namespace verwendet wird, aus dem das Objekt abgerufen wurde.

Für Microsoft-Gebiets Schema Bezeichner ist das Format der Zeichenfolge "MS \_ xxxx", wobei xxxx eine Zeichenfolge im hexadezimalen Format ist, die die LCID angibt. Der Gebiets Schema Bezeichner Deutschland ist beispielsweise "MS \_ 409".

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Austausch Pfad<br/>                                                       |
| IID<br/>                      | IID \_ iswbemubjectpath<br/>                                                        |



 

 




