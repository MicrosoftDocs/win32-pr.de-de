---
title: IReferenceClock-Methode ohne Empfehlung
description: Mit der unempfehlung-Methode wird eine Benachrichtigungs Anforderung abgebrochen.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Unempfehlung-Methode Windows Media-Format
- Unempfehlung-Methode Windows Media-Format, IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle Windows Media-Format, unempfehlung-Methode
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104101007"
---
# <a name="ireferenceclockunadvise-method"></a>IReferenceClock:: unempfehlung-Methode

Mit der **unempfehlung** -Methode wird eine Benachrichtigungs Anforderung abgebrochen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwadviabcookie* 
</dt> <dd>

Der Bezeichner der zu entfernenden Anforderung. Verwenden Sie den Wert, der von adviendtime im pdwadviscookie-Parameter zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Methode wurde erfolgreich ausgeführt.<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | Der-Bezeichner ist nicht vorhanden.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IReferenceClock-Schnittstelle**](ireferenceclock.md)
</dt> </dl>

 

 





