---
description: Die findmediafile-Methode sucht nach einer Datei und ruft, wenn erfolgreich, den Pfad zur Datei ab.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'Imedialocator:: findmediafile-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369414"
---
# <a name="imedialocatorfindmediafile-method"></a>Imedialocator:: findmediafile-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `FindMediaFile` -Methode sucht nach einer Datei und ruft, wenn erfolgreich, den Pfad zur Datei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Input* (Eingabe) 
</dt> <dd>

Dateiname, einschließlich des Pfads, in dem die Datei zuletzt bekannt war. Verwenden Sie für Quell Objekte in der Zeitachse den Namen des aktuellen Mediums.

</dd> <dt>

*Filter Zeichenfolge* 
</dt> <dd>

Ein **BSTR** , das Paare von Filter Zeichenfolgen enthält, die entsprechend dem **lpstrfilter** -Member der [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur formatiert sind. Der medienlocator verwendet diesen Filter, wenn ein Dialogfeld zum Öffnen von Dateien angezeigt wird. Der Wert kann **null** sein, wenn der *Flags* -Parameter das SFN \_ validatef-Popup Kennzeichen nicht enthält \_ .

</dd> <dt>

*poutput* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den eigentlichen Pfad zur Datei empfängt, wenn Sie sich von dem in der *Eingabe* enthaltenen Wert unterscheidet und die Methode die Datei erfolgreich findet.

</dd> <dt>

*Flags* 
</dt> <dd>

Bitweise Kombination von 0 (null) oder mehr Flags. Eine Liste möglicher Flags finden Sie unter [**Validierungsflags für Dateinamen**](file-name-validation-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die Filter Zeichenfolge für das Dialogfeld zum Öffnen von Dateien, das durch den *filterstring* -Parameter angegeben wird, enthält interne NULL-Zeichen. Video \\ 0 \* . avi \\ 0 \\ 0 ist beispielsweise eine gültige Filter Zeichenfolge. Sie können den BSTR nicht mithilfe der **sysallocstr** -Funktion zuordnen, da diese Funktion eine NULL-terminierte Zeichenfolge erwartet und die Zeichenfolge beim ersten NULL-Zeichen abschneidet. Verwenden Sie daher eine Funktion wie z. b. " **SysAllocStringLen**", die einen expliziten Parameter für die Länge enthält:


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



Wenn der Benutzer das Dialogfeld zum Öffnen von Dateien abbricht, gibt die Methode E \_ Fail zurück.

Die-Methode ordnet Speicher für **BSTR** in *poutput* zu. Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.

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

[**Imedialocator-Schnittstelle**](imedialocator.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 
