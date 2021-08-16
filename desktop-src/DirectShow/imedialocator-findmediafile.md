---
description: Die FindMediaFile-Methode sucht nach einer Datei und ruft bei Erfolg den Pfad zur Datei ab.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: IMediaLocator::FindMediaFile-Methode (Qedit.h)
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
ms.openlocfilehash: cc1acda4a3bc6e2d93ae8b7024ef34f759c11c5c4d487a09d3be3a3542e0c445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818937"
---
# <a name="imedialocatorfindmediafile-method"></a>IMediaLocator::FindMediaFile-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Methode sucht nach einer Datei und ruft bei Erfolg `FindMediaFile` den Pfad zur Datei ab.

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

Dateiname, einschließlich Pfad, in dem sich die Datei zuletzt befindet. Verwenden Sie für Quellobjekte auf der Zeitachse den aktuellen Mediennamen.

</dd> <dt>

*FilterString* 
</dt> <dd>

Ein **BSTR mit** Paaren von Filterzeichenfolgen, formatiert nach Bedarf für den **lpstrFilter-Member** der [**OPENFILENAME-Struktur.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Der Medienlocator verwendet diesen Filter, wenn ein Dialogfeld Datei öffnen angezeigt wird. Der Wert kann NULL **sein,** wenn *der Flags-Parameter* das SFN \_ VALIDATEF \_ POPUP-Flag nicht enthält.

</dd> <dt>

*pOutput* 
</dt> <dd>

Zeiger auf eine Variable, die den tatsächlichen Pfad zur Datei empfängt, wenn sie sich vom Wert in *Input* unterscheidet und die Methode die Datei erfolgreich findet.

</dd> <dt>

*Flags* 
</dt> <dd>

Bitweise Kombination von null oder mehr Flags. Eine Liste der möglichen Flags finden Sie unter [**Dateinamenvalidierungsflags**](file-name-validation-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die Filterzeichenfolge für das Dialogfeld Datei öffnen, das durch den *FilterString-Parameter* angegeben wird, enthält interne NULL-Zeichen. Beispielsweise ist Video \\ 0 \*.avi\\ 0 \\ 0 eine gültige Filterzeichenfolge. Sie können die **SysAllocStr-Funktion** nicht zum Zuordnen des BSTR verwenden, da diese Funktion eine auf NULL terminierte Zeichenfolge erwartet und die Zeichenfolge beim ersten NULL-Zeichen abschneiden wird. Verwenden Sie daher eine Funktion wie **SysAllocStringLen,** die einen expliziten Parameter für die Länge enthält:


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



Wenn der Benutzer das Dialogfeld Datei öffnen abbricht, gibt die Methode E \_ FAIL zurück.

Die -Methode weist Arbeitsspeicher für den **BSTR** in *pOutput zu.* Die Anwendung muss **SysFreeString aufrufen,** um den Arbeitsspeicher frei zu machen.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaLocator-Schnittstelle**](imedialocator.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 
