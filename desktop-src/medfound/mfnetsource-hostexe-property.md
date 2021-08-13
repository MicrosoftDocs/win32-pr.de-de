---
description: Der Wert des &Felds \# 0034;c-hostexe&\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: MFNETSOURCE_HOSTEXE-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dbde4b4b445e88a0cb6e7ebe45b8b88f386c208854057f209d9c36b7e0024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463650"
---
# <a name="mfnetsource_hostexe-property"></a>MFNETSOURCE \_ HOSTEXE-Eigenschaft

Der Wert des Felds "c-hostexe", das die Netzwerkquelle für die Protokollierung verwendet. Anwendungen können diese Eigenschaft auf den Namen der Hostanwendung festlegen. Der Wert kann beispielsweise "iexplore.exe" sein, wenn die Anwendung auf einer Webseite gehostet wird.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Breitzeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ HOSTEXE** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore-Zeiger** an den Quell resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientprotokollierung](client-logging.md)
</dt> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




