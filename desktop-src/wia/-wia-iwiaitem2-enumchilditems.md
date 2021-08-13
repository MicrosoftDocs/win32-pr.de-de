---
description: Erstellt ein Enumeratorobjekt und übergibt einen Zeiger auf seine IEnumWiaItem2-Schnittstelle für Ordner mit Elementen in der IWiaItem2-Struktur eines Windows Wia 2.0-Geräts.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: IWiaItem2::EnumChildItems-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 921a6b6e85f906ef62683038b2bb28dd484d58fd20600b2ff85ae594fafb3cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440418"
---
# <a name="iwiaitem2enumchilditems-method"></a>IWiaItem2::EnumChildItems-Methode

Erstellt ein Enumeratorobjekt und übergibt einen Zeiger auf seine [**IEnumWiaItem2-Schnittstelle**](-wia-ienumwiaitem2.md) für Ordner mit Elementen in der [**IWiaItem2-Struktur**](-wia-iwiaitem2.md) eines Windows WIA 2.0-Geräts (Image Acquisition).

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCategoryGUID* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Gibt einen Zeiger auf eine Kategorie an, für die untergeordnete Knoten aufzählt werden. Wenn **NULL** ist, werden alle untergeordneten Knoten aufzählt.

</dd> <dt>

*ppIEnumWiaItem2* \[ out\]
</dt> <dd>

Typ: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IEnumWiaItem2-Schnittstelle,**](-wia-ienumwiaitem2.md) die von dieser Methode erstellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das WIA 2.0-Laufzeitsystem stellt jedes WIA 2.0-Hardwaregerät als hierarchische Struktur von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) dar. Mit der **IWiaItem2::EnumChildItems-Methode** können Anwendungen untergeordnete Elemente im aktuellen Element auflisten. Sie kann jedoch nur auf Elemente angewendet werden, die Ordner sind.

Wenn der Ordner nicht leer ist, enthält er eine Unterstruktur von [**IWiaItem2-Objekten.**](-wia-iwiaitem2.md) Die **IWiaItem2::EnumChildItems-Methode** listet alle elemente auf, die im Ordner enthalten sind. Es speichert einen Zeiger auf einen Enumerator im *ppIEnumWiaItem2-Parameter.* Anwendungen verwenden den Enumeratorzeiger, um die Enumeration der untergeordneten Elemente eines Objekts auszuführen.

Anwendungen müssen die [IUnknown::Release-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die Schnittstellenzeiger aufrufen, die sie über den *ppIEnumWiaItem2-Parameter* empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
