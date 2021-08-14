---
title: INapSoHProcessor-Schnittstelle (NapProtocol.h)
description: Werden von SHAs verwendet, um den Inhalt von SoHResponses zu verarbeiten, und von SHVs, um den Inhalt von SoHRequests zu verarbeiten.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- INapSoHProcessor-Schnittstelle NAP
- INapSoHProcessor-Schnittstelle NAP , beschrieben
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
ms.openlocfilehash: ca4a87e15d3810605038231eaec066e9f26ed079aca0d0715c72e7c69ed8d600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799482"
---
# <a name="inapsohprocessor-interface"></a>INapSoHProcessor-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**Der INapSoHProcessor** stellt Methoden bereit, die von SHAs zum Verarbeiten des Inhalts von [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) und von SHVs verwendet werden, um den Inhalt von **SoHRequests** zu verarbeiten.

## <a name="members"></a>Member

Die **INapSoHProcessor-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSoHProcessor** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSoHProcessor-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                           | BESCHREIBUNG                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)         | Sucht den Speicherortindex des nächsten SoH-Paketattributs.<br/>                 |
| [**INapSoHProcessor::GetAttribute**](inapsohprocessor-getattribute-method.md)                   | Ruft den Attributtyp und -wert ab.<br/>                                    |
| [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md) | Ruft die Anzahl der im SoH enthaltenen Attribute ab.<br/>                   |
| [**INapSoHProcessor::Initialize**](inapsohprocessor-initialize-method.md)                       | Initialisiert das SoH-Protokollpaket und das NAP-System für die Inhaltsverarbeitung.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

