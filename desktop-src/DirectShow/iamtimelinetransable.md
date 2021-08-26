---
description: Die IAMTimelineTransable-Schnittstelle fügt einem Objekt in DirectShow Editing Services (DES) Übergänge hinzu.
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: IAMTimelineTransable-Schnittstelle (Qedit.h)
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
ms.openlocfilehash: 6228b836f85251dda7f43d6c3b421d486b727c6bdc6c319b9cf7ca1e37d34a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052030"
---
# <a name="iamtimelinetransable-interface"></a>IAMTimelineTransable-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `IAMTimelineTransable` -Schnittstelle fügt einem Objekt in [DirectShow Editing Services (DES) Übergänge](directshow-editing-services.md) hinzu. Diese Schnittstelle wird von jedem Objekt verfügbar gemacht, auf das Übergänge angewendet werden können, einschließlich Spuren, Kompositionen und Gruppen. Ein Objekt, das diese Schnittstelle implementiert, kann eine beliebige Anzahl von Übergängen haben, aber die Übergänge dürfen sich nicht zeitlich überschneiden.

> [!Note]  
> Audio unterstützt keine Übergänge. Objekte in Audiogruppen können die Schnittstelle verfügbar machen, aber die Anwendung sollte ihnen keine `IAMTimelineTransable` Übergänge hinzufügen.

 

## <a name="members"></a>Member

Die **IAMTimelineTransable-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTransable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMTimelineTransable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | Beschreibung                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetNextTrans**](iamtimelinetransable-getnexttrans.md)       | Ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | Ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird, mit der als **REFTIME-Wert angegebenen** Zeit.<br/> |
| [**GetTransAtTime**](iamtimelinetransable-gettransattime.md)   | Ruft den Übergang ab, der der angegebenen Zeit am nächsten ist.<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | Ruft den Übergang ab, der der angegebenen Zeit am nächsten ist, angegeben als **REFTIME-Wert.**<br/>                                   |
| [**TransAdd**](iamtimelinetransable-transadd.md)               | Fügt dem -Objekt einen Übergang hinzu.<br/>                                                                                        |
| [**TransGetCount**](iamtimelinetransable-transgetcount.md)     | Ruft die Anzahl der Übergänge für dieses Objekt ab.<br/>                                                                     |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
