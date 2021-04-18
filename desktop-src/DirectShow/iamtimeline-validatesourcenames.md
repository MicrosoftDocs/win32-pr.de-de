---
description: Die validatesourcenames-Methode überprüft die Quellnamen in der Zeitachse mithilfe des medienlocators. Diese Methode aktualisiert optional auch jedes Quell Objekt, für das es eine Datei sucht.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'Iamtimeline:: validatesourcenames-Methode (qedit. h)'
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
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360922"
---
# <a name="iamtimelinevalidatesourcenames-method"></a>Iamtimeline:: validatesourcenames-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `ValidateSourceNames` Methode überprüft die Quellnamen in der Zeitachse mithilfe des medienlocators. Diese Methode aktualisiert optional auch jedes Quell Objekt, für das es eine Datei sucht.

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

*Validateflags* 
</dt> <dd>

Bitweise Kombination von [**Dateinamens-Validierungsflags**](file-name-validation-flags.md) , die das Verhalten des medienlocators angeben. Die SFN \_ validatef \_ Replace-und SFN \_ validatef- \_ prüfflags müssen vorhanden sein, oder die Methode gibt E \_ invalidArg zurück.

</dd> <dt>

*poverride* 
</dt> <dd>

Optionaler Zeiger auf die [**imedialocator**](imedialocator.md) -Schnittstelle eines medienlocators, der anstelle der Standardeinstellung verwendet werden soll. Legen Sie den Wert dieses Parameters auf **null** fest, um den standardmedienlocator zu verwenden. Weitere Informationen finden Sie unter Hinweise.

</dd> <dt>

*Notierter benachrichtigsthread* 
</dt> <dd>

Handle für ein Ereignis. Die-Methode signalisiert das-Ereignis, nachdem die Überprüfung abgeschlossen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Mithilfe des Parameters " *poverride* " können Sie eine eigene benutzerdefinierte Implementierung der [**imedialocator**](imedialocator.md) -Schnittstelle bereitstellen. Der standardmäßige medienlocator benachrichtigt Ihre Anwendung z. b. nicht über die gefundenen Dateien (oder kann nicht gefunden werden). Um diese Einschränkung zu umgehen, können Sie einen benutzerdefinierten medienlocator implementieren, der als Wrapper für die Standardversion definiert ist. Übergeben Sie in der benutzerdefinierten Version [**imedialocator:: findmediafile**](imedialocator-findmediafile.md) -Aufrufe direkt an die Standardversion, und überprüfen Sie den Rückgabewert.

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

[**Iamtimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




