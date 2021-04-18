---
description: Die iamtimelinetrans-Schnittstelle stellt Methoden zum Bearbeiten von Übergängen in DirectShow-Bearbeitungs Diensten bereit.
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Iamtimelinetrans-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365805"
---
# <a name="iamtimelinetrans-interface"></a>Iamtimelinetrans-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IAMTimelineTrans` Schnittstelle stellt Methoden zum Ändern von Übergängen in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit. Ein Übergang ist ein Fortschritt zwischen einer Video Ebene und dem gerenderten zusammengesetzten aller Video Ebenen mit niedrigerer Priorität. Einem Zeitachsen Objekt, das die [**iamtimelinetransable**](iamtimelinetransable.md) -Schnittstelle verfügbar macht, kann ein Übergang hinzugefügt werden. Um Eigenschaften für einen Übergang festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.

Das des-Übergangs Objekt ist tatsächlich ein Wrapper für ein DirectX-Transformations Objekt. Ein DirectX-Transformations Objekt mit 2 Eingaben kann verwendet werden, um den visuellen Effekt für den Übergang zu implementieren. Microsoft unterstützt die Entwicklung von DirectX-Transformations Objekten von Drittanbietern nicht mehr. Um das DirectX-Transformations Objekt für einen Übergang anzugeben, müssen Sie die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode aufrufen.

Um ein Übergangs Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert der Zeitachsen \_ \_ Haupttyp auf \_ . Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die- `IAMTimelineTrans` Schnittstelle Abfragen.

## <a name="members"></a>Member

Die **iamtimelinetrans** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelinetrans** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelinetrans** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Getcutpoint**](iamtimelinetrans-getcutpoint.md)     | Ruft den Ausschneide Punkt ab.<br/>                                                    |
| [**GetCutPoint2**](iamtimelinetrans-getcutpoint2.md)   | Ruft den Ausschneide Punkt als [**ref-Zeit**](reftime.md) Wert ab.<br/>             |
| [**Getcutsonly**](iamtimelinetrans-getcutsonly.md)     | Bestimmt, ob der Übergang als Ausschneide gerendert wird.<br/>                     |
| [**Ge-wapinputs**](iamtimelinetrans-getswapinputs.md) | Ruft einen Wert ab, der angibt, ob die Übergangs Eingaben ausgetauscht werden.<br/> |
| [**Setcutpoint**](iamtimelinetrans-setcutpoint.md)     | Legt den Ausschneide Punkt fest.<br/>                                                         |
| [**SetCutPoint2**](iamtimelinetrans-setcutpoint2.md)   | Legt den Ausschneide Punkt als [**ref**](reftime.md) -Zeitwert fest.<br/>                  |
| [**Setcutsonly**](iamtimelinetrans-setcutsonly.md)     | Gibt an, ob der Übergang als Ausschneide gerendert wird.<br/>                      |
| [**"-Wapinputs"**](iamtimelinetrans-setswapinputs.md) | Gibt an, ob die Übergangs Eingaben ausgetauscht werden.<br/>                        |



 

## <a name="remarks"></a>Bemerkungen

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

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
