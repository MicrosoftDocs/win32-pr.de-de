---
description: Die effectinsbefore-Methode fügt einen Effekt auf der angegebenen Prioritäts Ebene in das-Objekt ein.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'Iamtimelineeffectable:: effectinsbefore-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369295"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>Iamtimelineeffectable:: effectinsbefore-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `EffectInsBefore` Methode fügt einen Effekt auf der angegebenen Prioritäts Ebene in das-Objekt ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PFX* 
</dt> <dd>

Ein Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Effekts.

</dd> <dt>

*Priority* 
</dt> <dd>

Prioritätsstufe, bei der der Effekt eingefügt werden soll. Verwenden Sie den Wert – 1, um den Effekt am Ende der Prioritäts Liste einzufügen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück, oder E benachrichtigt, \_ Wenn das Objekt nicht wirksam ist. Andernfalls wird ein anderer **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Die Start-und Endzeiten des Effekts werden bei Bedarf innerhalb der Grenzen des-Zeit Bereichs des Objekts abgeschnitten. Wenn bereits ein Effekt auf der angegebenen Prioritätsstufe vorliegt, werden alle Effekte von diesem Punkt auf der Prioritäts Liste nach unten verschoben, um Platz für den neuen Effekt zu schaffen.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelineeffectable-Schnittstelle**](iamtimelineeffectable.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




