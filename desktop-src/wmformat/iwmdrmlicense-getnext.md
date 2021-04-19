---
title: Iwmdrmlicense GetNext-Methode (wmdrmsdk. h)
description: Die GetNext-Methode lädt die Informationen zum nächsten Element in der Liste.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- GetNext-Methode (Windows Media-Format)
- GetNext-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, GetNext-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354092"
---
# <a name="iwmdrmlicensegetnext-method"></a>Iwmdrmlicense:: GetNext-Methode

Die **GetNext** -Methode lädt die Informationen zum nächsten Element in der Liste.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNext();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt> </dl> | Es wird eine aktualisierte Inhalts Sperr Liste benötigt.<br/> |
| <dl> <dt>**Fehler \_ keine \_ weiteren \_ Elemente**</dt> </dl>      | In der Liste sind keine Elemente mehr vorhanden.<br/>          |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Die Methoden der [**iwmdrmlicense**](iwmdrmlicense.md) -Schnittstelle stellen jeweils Daten zu einer einzelnen Lizenz bereit. Das zugrunde liegende-Objekt enthält eine Liste mit mindestens einer Lizenz. Wenn Sie diese Methode aufgerufen haben, verschiebt die-Schnittstelle Ihre internen Verweise auf die nächste Lizenz in der Liste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





