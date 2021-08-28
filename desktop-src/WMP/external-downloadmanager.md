---
title: External.DownloadManager
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die DownloadManager-Eigenschaft ruft das DownloadManager-Objekt ab.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- External.DownloadManager-Windows Media Player
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
ms.openlocfilehash: 2d828435c43f57406e637312245b2bb3ae3e7c35510c9b2daf478a7fec39b599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649210"
---
# <a name="externaldownloadmanager"></a>External.DownloadManager

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **DownloadManager-Eigenschaft** ruft das **DownloadManager-Objekt** ab.

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein schreibgeschütztes **DownloadManager-Objekt.**

## <a name="remarks"></a>Hinweise

In Windows Media Player 10 oder höher sind **die DownloadManager-Eigenschaft** und das -Objekt nur über Aufgabenbereiche des Onlineshopdiensts zugänglich. DownloadManager kann nicht **von anderen** Features verwendet werden, für die das **Externe** Objekt verfügbar ist, z. B. HTMLView, Info Center View und Albuminformationen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





