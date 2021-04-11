---
title: Inapsohprocessor-Schnittstelle (napprotocol. h)
description: Werden von SHAs verwendet, um den Inhalt von sohantworten und von SHVs zu verarbeiten, um den Inhalt von sohrequests zu verarbeiten.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- Inapsohprocessor-Schnittstelle NAP
- Inapsohprocessor-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040132"
---
# <a name="inapsohprocessor-interface"></a>Inapsohprocessor-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Der **inapsohprocessor** stellt Methoden bereit, die von SHAs zum Verarbeiten des Inhalts von [**sohantworten**](/windows/win32/api/naptypes/ns-naptypes-soh) und von SHVs verwendet werden, um den Inhalt von **sohrequests** zu verarbeiten.

## <a name="members"></a>Member

Die **inapsohprocessor** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapsohprocessor** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapsohprocessor** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                           | BESCHREIBUNG                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Inapsohprocessor:: findnextattribute**](inapsohprocessor-findnextattribute-method.md)         | Sucht den Speicherort Index des nächsten SoH-Paket Attributs.<br/>                 |
| [**Inapsohprocessor:: GetAttribute**](inapsohprocessor-getattribute-method.md)                   | Ruft den Attributtyp und-Wert ab.<br/>                                    |
| [**Inapsohprocessor:: getnumofattributes**](inapsohprocessor-getnumberofattributes-method.md) | Ruft die Anzahl der im SoH enthaltenen Attribute ab.<br/>                   |
| [**Inapsohprocessor:: Initialize**](inapsohprocessor-initialize-method.md)                       | Initialisiert das SoH-Protokoll Paket und das NAP-System für die Inhalts Verarbeitung.<br/> |



 

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

 

