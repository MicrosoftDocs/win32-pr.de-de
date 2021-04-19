---
description: Die imedialocator-Schnittstelle stellt Methoden zum Validieren von Dateinamen in DirectShow-Bearbeitungs Diensten bereit.
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Imedialocator-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366891"
---
# <a name="imedialocator-interface"></a>Imedialocator-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IMediaLocator` Schnittstelle stellt Methoden zum Validieren von Dateinamen in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit. Verwenden Sie diese Schnittstelle, um sicherzustellen, dass der angegebene Dateiname und der Pfad einer vorhandenen Datei entsprechen. Diese Schnittstelle bietet auch eine Möglichkeit, um an anderen Speicherorten nach der Datei zu suchen und ein Dialogfeld **Öffnen** anzuzeigen, in dem der Benutzer die Datei finden kann.

Der medienlocator implementiert diese Schnittstelle. Die Zeitachse und die Rendering-Engine unterstützen auch die Überprüfung von Dateinamen mithilfe der folgenden Methoden:

-   [**Iamtimeline:: validatesourcenames**](iamtimeline-validatesourcenames.md): überprüft und aktualisiert Dateinamen in der Zeitachse.
-   [**Alienderengine:: setsourcenamevalidation**](irenderengine-setsourcenamevalidation.md): gibt an, wie die Renderingengine Dateinamen zur Renderingzeit überprüft.

In der Regel wird diese Methode von einer des-Anwendung aufgerufen, anstatt direkt eine Instanz des medienlocators zu erstellen. Weitere Informationen finden Sie unter [using the Media Locator](using-the-media-locator.md).

## <a name="members"></a>Member

Die **imedialocator** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imedialocator** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imedialocator** -Schnittstelle verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**Addfoundlocation**](imedialocator-addfoundlocation.md) | Fügt dem Verzeichnis Cache ein Verzeichnis hinzu.<br/>                                |
| [**Findmediafile**](imedialocator-findmediafile.md)       | Sucht nach einer Datei und ruft, wenn erfolgreich, den Pfad zur Datei ab.<br/> |



 

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



 

 
