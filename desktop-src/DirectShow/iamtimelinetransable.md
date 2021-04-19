---
description: Die iamtimelinetransable-Schnittstelle fügt Übergänge zu einem Objekt in DirectShow-Bearbeitungs Diensten (des) hinzu.
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Iamtimelinetransable-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371331"
---
# <a name="iamtimelinetransable-interface"></a>Iamtimelinetransable-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IAMTimelineTransable` Schnittstelle fügt Übergänge zu einem Objekt in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) hinzu. Diese Schnittstelle wird von jedem Objekt verfügbar gemacht, auf das Übergänge angewendet werden können, einschließlich der Spuren, der Komposition und der Gruppen. Ein Objekt, das diese Schnittstelle implementiert, kann über eine beliebige Anzahl von Übergängen verfügen, aber die Übergänge dürfen sich nicht rechtzeitig überlappen.

> [!Note]  
> Das Audioformat unterstützt keine Übergänge. Objekte in Audiogruppen können die- `IAMTimelineTransable` Schnittstelle verfügbar machen, aber die Anwendung sollte Ihnen keine Übergänge hinzufügen.

 

## <a name="members"></a>Member

Die **iamtimelinetransable** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelinetransable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelinetransable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Getnexttrans**](iamtimelinetransable-getnexttrans.md)       | Ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird, wobei die Zeit als **ref Time** -Wert angegeben wird.<br/> |
| [**Gettransattime**](iamtimelinetransable-gettransattime.md)   | Ruft den Übergang ab, der dem angegebenen Zeitpunkt am nächsten liegt.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Ruft den Übergang ab, der dem angegebenen Zeitpunkt am nächsten liegt, der als **reftime** -Wert angegeben wird.<br/>                                   |
| [**Transadd**](iamtimelinetransable-transadd.md)               | Fügt dem-Objekt einen Übergang hinzu.<br/>                                                                                        |
| [**Transgetcount**](iamtimelinetransable-transgetcount.md)     | Ruft die Anzahl der Übergänge für dieses-Objekt ab.<br/>                                                                     |



 

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



 

 
