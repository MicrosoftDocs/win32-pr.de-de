---
description: Erstellt ein Enumeratorobjekt und übergibt einen Zeiger auf seine IEnumWiaItem2-Schnittstelle für Ordner mit Elementen in der IWiaItem2-Struktur eines Windows-Abbild Erwerbs (WIA) 2,0-Geräts.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'IWiaItem2:: enumchilditems-Methode (WIA. h)'
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
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485067"
---
# <a name="iwiaitem2enumchilditems-method"></a>IWiaItem2:: enumchilditems-Methode

Erstellt ein Enumeratorobjekt und übergibt einen Zeiger auf seine [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) -Schnittstelle für Ordner mit Elementen in der [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur eines Windows-Abbild Erwerbs (WIA) 2,0-Geräts.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcategoryguid* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *GUID \** _

Gibt einen Zeiger auf eine Kategorie an, für die untergeordnete Knoten aufgelistet werden. Wenn _ * NULL * *, werden alle untergeordneten Knoten aufgelistet.

</dd> <dt>

*ppIEnumWiaItem2* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) -Schnittstelle, die von dieser Methode erstellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das WIA 2,0-Laufzeitsystem stellt jedes WIA 2,0-Hardware Gerät als hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten dar. Mit der **IWiaItem2:: enumchilditems** -Methode können Anwendungen untergeordnete Elemente im aktuellen Element aufzählen. Sie kann jedoch nur auf Elemente angewendet werden, bei denen es sich um Ordner handelt.

Wenn der Ordner nicht leer ist, enthält er eine Teilstruktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten. Mit der **IWiaItem2:: enumchilditems** -Methode werden alle im Ordner enthaltenen Elemente aufgelistet. Es speichert einen Zeiger auf einen Enumerator im *ppIEnumWiaItem2* -Parameter. Anwendungen verwenden den enumeratorzeiger, um die Enumeration der untergeordneten Elemente eines Objekts auszuführen.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppIEnumWiaItem2* -Parameter empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
