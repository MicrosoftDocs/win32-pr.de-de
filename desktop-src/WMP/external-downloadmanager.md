---
title: Extern. Download Manager
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Download Manager-Eigenschaft ruft das Download Manager-Objekt ab.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- Externe. Download Manager-Windows-Media Player
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370127"
---
# <a name="externaldownloadmanager"></a>Extern. Download Manager

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **Download Manager** -Eigenschaft ruft das **Download Manager** -Objekt ab.

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein Schreib geschütztes **Download Manager** -Objekt.

## <a name="remarks"></a>Bemerkungen

In Windows Media Player 10 oder höher sind die **Download Manager** -Eigenschaft und das-Objekt nur über Aufgabenbereiche des Online Store Service zugänglich. Sie können den **Download Manager** nicht aus anderen Features verwenden, bei denen das **externe** Objekt verfügbar ist, z. b. HtmlView, Info Center View und Album-Informationen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 2-Online Speicher**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





