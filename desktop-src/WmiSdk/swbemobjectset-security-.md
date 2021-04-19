---
description: Die Security- \_ Eigenschaft des errbewbjectset-Objekts wird verwendet, um die Sicherheitseinstellungen für ein errbewbjectset-Objekt zu erhalten oder festzulegen. Diese Eigenschaft ist ein Swap Security-Objekt.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: SWbemObjectSet.Security_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348523"
---
# <a name="swbemobjectsetsecurity_-property"></a>Errbemubjectset. Security- \_ Eigenschaft

Die **Security \_** -Eigenschaft des [**errbewbjectset**](swbemobjectset.md) -Objekts wird verwendet, um die Sicherheitseinstellungen für ein **errbewbjectset** -Objekt zu erhalten oder festzulegen. Diese Eigenschaft ist ein [**Swap Security**](swbemsecurity.md) -Objekt.

> [!Note]  
> Das Festlegen [**der \_ Security**](swbemobject-security-.md) -Eigenschaft eines ' [**errbemubjectset**](swbemobjectset.md) '-Objekts auf **null** gewährt allen Benutzern jederzeit uneingeschränkten Zugriff. Weitere Informationen zu den Auswirkungen des unbegrenzten Zugriffs finden Sie unter [**Swap Security**](swbemsecurity.md).

 

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectSet.Security_ As Object
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
| CLSID<br/>                    | CLSID- \_ Swap-Objekt Satz<br/>                                                        |
| IID<br/>                      | IID \_ iswbemubjectset<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austauschen von "errbemubjectset"**](swbemobjectset.md)
</dt> <dt>

[Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Sichern von Skript Clients](securing-scripting-clients.md)
</dt> </dl>

 

 




