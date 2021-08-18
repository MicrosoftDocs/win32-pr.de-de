---
description: Die ValidateSourceNames-Methode überprüft Quellnamen auf der Zeitachse mithilfe des Medienlocators. Optional aktualisiert diese Methode auch alle Quellobjekte, für die sie eine Datei sucht.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: IAMTimeline::ValidateSourceNames-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cabaa5f9ec67abaf8805ad55917d0a33b6ad3457bedd8899b3f443f1a247b8d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043110"
---
# <a name="iamtimelinevalidatesourcenames-method"></a>IAMTimeline::ValidateSourceNames-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `ValidateSourceNames` -Methode überprüft Quellnamen auf der Zeitachse mithilfe des Medienlocators. Optional aktualisiert diese Methode auch alle Quellobjekte, für die sie eine Datei sucht.

## <a name="syntax"></a>Syntax


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ValidateFlags* 
</dt> <dd>

Bitweise Kombination von [**Dateinamenvalidierungsflags,**](file-name-validation-flags.md) die das Verhalten des Medienlocators angeben. Die SFN \_ VALIDATEF \_ REPLACE- und SFN \_ VALIDATEF \_ CHECK-Flags müssen vorhanden sein, andernfalls gibt die Methode E \_ INVALIDARG zurück.

</dd> <dt>

*pOverride* 
</dt> <dd>

Optionaler Zeiger auf die [**IMediaLocator-Schnittstelle**](imedialocator.md) eines Medienlocators, der anstelle des Standardwerts verwendet werden soll. Um den Standardmedienlocator zu verwenden, legen Sie den Wert dieses Parameters auf **NULL** fest. Weitere Informationen finden Sie unter Hinweise.

</dd> <dt>

*NotifyEventHandle* 
</dt> <dd>

Handle für ein Ereignis. Die -Methode signalisiert das Ereignis, nachdem die Überprüfung abgeschlossen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Mit dem *pOverride-Parameter* können Sie Ihre eigene benutzerdefinierte Implementierung der [**IMediaLocator-Schnittstelle**](imedialocator.md) bereitstellen. Beispielsweise benachrichtigt der Standardmedienlocator Ihre Anwendung nicht über die gefundenen (oder nicht gefundenen) Dateien. Um diese Einschränkung zu umgehen, könnten Sie einen benutzerdefinierten Medienlocator implementieren, sodass er als Wrapper für die Standardversion verwendet wird. Übergeben Sie in Ihrer benutzerdefinierten Version [**IMediaLocator::FindMediaFile-Aufrufe**](imedialocator-findmediafile.md) direkt an die Standardversion, und überprüfen Sie den Rückgabewert.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




