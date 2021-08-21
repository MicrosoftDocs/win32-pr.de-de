---
description: Enthält das Anwendungsobjekt des Ordners.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Folder.Application-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 41c0c3efd2664e7f3544ee5f58e4e1c530d97ca7ef754030c082103598011a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860355"
---
# <a name="folderapplication-property"></a>Folder.Application-Eigenschaft

Enthält das Anwendungsobjekt des Ordners.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Application = Folder.Application
```



## <a name="property-value"></a>Eigenschaftswert

Ein Objektverweis auf das Application-Objekt.

## <a name="remarks"></a>Hinweise

Die **Application-Eigenschaft** gibt das Automatisierungsobjekt zurück, das von der Anwendung unterstützt wird, die das WebBrowser-Steuerelement enthält, wenn auf dieses Objekt zugegriffen werden kann. Andernfalls gibt diese Eigenschaft das Automatisierungsobjekt des WebBrowser-Steuerelements zurück.

Verwenden Sie diese Eigenschaft mit den Befehlen **Set** und **CreateObject** oder mit dem **Befehl GetObject,** um eine Instanz der Internet Explorer Anwendung zu erstellen und zu bearbeiten.

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise wird die [**ParseName-Methode**](folder-parsename.md) nicht für den ordner Systemsteuerung (CSIDL \_ CONTROLS) implementiert. Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800A01BD (Dezimalzahl 445) ausgelöst.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                 |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




