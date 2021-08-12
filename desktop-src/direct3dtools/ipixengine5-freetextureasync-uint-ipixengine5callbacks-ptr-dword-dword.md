---
description: Gibt eine Textur frei und benachrichtigt den Host asynchron.
MS-HAID: vspixengine.IPixEngine5\_FreeTextureAsync\_UINT\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5::FreeTextureAsync-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A2D46D4-AA09-4E50-8109-774CE7F538E7
api_name:
- IPixEngine5.FreeTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58ce1718abe75e2a3a992ce4a215c6bad280d7bd7de5e59f4117feaa8d475383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282829"
---
# <a name="span-idvspixengineipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dwordspanipixengine5freetextureasync-method"></a><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::FreeTextureAsync-Methode

Gibt eine Textur frei und benachrichtigt den Host asynchron.

## <a name="syntax"></a>Syntax


```C++
HRESULT FreeTextureAsync(
   UINT                  textureId,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*textureId*   
Die ID der Freitextur.

*Rückrufe*   
Die Adresse eines Objekts, das die IPixEngine5-Rückrufschnittstelle anordnt.

*requestCookie*   
Ein Cookie, das die Anforderung eindeutig idenfiiert und verwendet werden kann, um zu signalisieren, dass sie abgebrochen wird.

*progressIntervalMsecs*   
Wird nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
