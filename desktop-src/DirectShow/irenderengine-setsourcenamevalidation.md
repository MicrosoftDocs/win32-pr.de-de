---
description: Die setsourcenamevalidation-Methode gibt an, wie Dateinamen von der Renderingengine überprüft werden.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'Unenderengine:: setsourcenamevalidation-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360953"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a>Unenderengine:: setsourcenamevalidation-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetSourceNameValidation` Methode gibt an, wie Dateinamen von der Renderingengine überprüft werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Filter Zeichenfolge* 
</dt> <dd>

**BSTR** -Wert, der Paare von Filter Zeichenfolgen enthält, die entsprechend dem **lpstrfilter** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur formatiert sind. Der medienlocator verwendet diesen Filter, wenn dem Endbenutzer ein Dialogfeld "Datei öffnen" angezeigt wird.

</dd> <dt>

*poverride* 
</dt> <dd>

Optionaler Zeiger auf die [**imedialocator**](imedialocator.md) -Schnittstelle eines medienlocators, der anstelle der Standardeinstellung verwendet werden soll. Legen Sie den Wert dieses Parameters auf **null** fest, um den standardmedienlocator zu verwenden. Weitere Informationen finden Sie unter Hinweise.

</dd> <dt>

*Flags* 
</dt> <dd>

Bitweise Kombination von [**Dateinamens-Validierungsflags**](file-name-validation-flags.md) , die das Verhalten des medienlocators angeben. Das Check-Flag von SFN \_ validatef \_ muss vorhanden sein. Das Flag SFN \_ validatef \_ hlinkgedämpfhat keine Auswirkung auf diese Methode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**E \_ muss \_ Init \_ Renderer**</dt> </dl> | Fehler beim Initialisieren der Rendering-Engine.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Mithilfe des Parameters " *poverride* " können Sie eine eigene benutzerdefinierte Implementierung der [**imedialocator**](imedialocator.md) -Schnittstelle bereitstellen. Beispielsweise benachrichtigt der Standard Medien-Serverlocatorpunkt eine Anwendung nicht über die gefundenen Dateien (oder kann nicht gefunden werden). Um diese Einschränkung zu umgehen, können Sie einen benutzerdefinierten medienlocator implementieren, der als Wrapper für die Standardversion definiert ist. Übergeben Sie dann [**imedialocator:: findmediafile**](imedialocator-findmediafile.md) -Aufrufe direkt an die Standardversion, und überprüfen Sie den Rückgabewert.

Derzeit werden von dieser Methode keine dynamisch geladenen Quellen überprüft. Weitere Informationen finden Sie unter " [**unenderengine:: setdynamikreconnectlevel**](irenderengine-setdynamicreconnectlevel.md)".

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

[**Schnittstelle ""**](irenderengine.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 
