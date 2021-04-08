---
title: Inapsohconstructor-Schnittstelle (napprotocol. h)
description: Werden von SHAs zum Erstellen von sohrequests und von SHVs zum Erstellen von sohantworten verwendet.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- Inapsohconstructor-Schnittstelle NAP
- Inapsohconstructor Interface NAP, beschrieben
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
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949479"
---
# <a name="inapsohconstructor-interface"></a>Inapsohconstructor-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Der **inapsohconstructor** stellt Methoden bereit, die von SHAs zum Erstellen von [**sohrequests**](/windows/win32/api/naptypes/ns-naptypes-soh) und von SHVs zum Erstellen von **sohantworten** verwendet werden.

## <a name="members"></a>Member

Die **inapsohconstructor** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapsohconstructor** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapsohconstructor** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [**Inapsohconstructor:: appendattribute**](inapsohconstructor-appendattribute-method.md) | Fügt ein TLV am Ende des SoH-Puffers hinzu.<br/> |
| [**Inapsohconstructor:: getsoh**](inapsohconstructor-getsoh-method.md)                   | Ruft das erstellte SoH-Paket ab.<br/>    |
| [**Inapsohconstructor:: Initialize**](inapsohconstructor-initialize-method.md)           | Initialisiert das SoH-Paket.<br/>              |
| [**Inapsohconstructor:: Validate**](inapsohconstructor-validate-method.md)               | Überprüft die Gültigkeit des SoH-Pakets.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Napprotocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napprotocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

