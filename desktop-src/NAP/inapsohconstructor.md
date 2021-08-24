---
title: INapSoHConstructor-Schnittstelle (NapProtocol.h)
description: Werden von SHAs zum Erstellen von SoHRequests und von SHVs zum Erstellen von SoHResponses verwendet.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- INapSoHConstructor-Schnittstelle NAP
- INapSoHConstructor-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ceb9e927e1ac65f21a3ff457922e1bd475b8327ac2525b2af7afefa6cb173f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037850"
---
# <a name="inapsohconstructor-interface"></a>INapSoHConstructor-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Der **INapSoHConstructor** bietet Methoden, die von SHAs zum Erstellen von [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) und von SHVs zum Erstellen von **SoHResponses verwendet werden.**

## <a name="members"></a>Member

Die **INapSoHConstructor-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSoHConstructor** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSoHConstructor-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [**INapSoHConstructor::AppendAttribute**](inapsohconstructor-appendattribute-method.md) | Fügt am Ende des SoH-Puffers einen TLV hinzu.<br/> |
| [**INapSoHConstructor::GetSoH**](inapsohconstructor-getsoh-method.md)                   | Ruft das konstruierte SoH-Paket ab.<br/>    |
| [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md)           | Initialisiert das SoH-Paket.<br/>              |
| [**INapSoHConstructor::Validate**](inapsohconstructor-validate-method.md)               | Überprüft die Gültigkeit des SoH-Pakets.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

