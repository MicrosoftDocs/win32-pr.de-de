---
title: TS_ATTRID (textstor. h)
description: Der TS \_ Atre-Datentyp wird verwendet, um ein Text Attribut zu identifizieren.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739784"
---
# <a name="ts_attrid"></a>TS \_ -attrd

Der **TS \_ Atre-** Datentyp wird verwendet, um ein Text Attribut zu identifizieren.


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a>Bemerkungen

Eine Liste vordefinierter GUIDs für TS \_ atdid ist in der Spalte ". h" enthalten.

Der GUIDs-Text " \_ \_ -Text verticalwriting" und die \_ Textausrichtung "-Text" \_ sind nützlich für Anwendungen, um den zu korrigierenden Eingabe Text abzugleichen. Es können zusätzliche benutzerdefinierte GUIDs erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                             |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITextStoreACP:: findnextattrtransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[**ITextStoreACP:: requestatus-satposition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[**ITextStoreACP:: requestatus-stransitioningatposition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreACP:: requestsupportedattrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[**ITextStoreACPSink:: onattrschange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[**Itextstoreanchor:: findnextattrtransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[**Itextstoreanchor:: requestatus-satposition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[**Itextstoreanchor:: requestatus-stransitioningatposition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[**Itextstoreanchor:: requestsupportedattrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[**Itextstoreanchorsink:: onattrschange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[**TS- \_ attrval**](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





