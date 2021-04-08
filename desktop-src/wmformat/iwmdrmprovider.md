---
title: Iwmdrmprovider-Schnittstelle
description: Die iwmdrmprovider-Schnittstelle stellt eine Methode bereit, mit der die anderen Objekte der erweiterten APIs für den Microsoft Windows Media DRM-Client erstellt werden. Sie können einen Zeiger auf eine Instanz dieser Schnittstelle abrufen, indem Sie die wmdrmcreateprovider-Funktion aufrufen.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Iwmdrmprovider-Schnittstelle Windows Media-Format
- Iwmdrmprovider-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729216"
---
# <a name="iwmdrmprovider-interface"></a>Iwmdrmprovider-Schnittstelle

Die **iwmdrmprovider** -Schnittstelle stellt eine Methode bereit, mit der die anderen Objekte der erweiterten APIs für den Microsoft Windows Media DRM-Client erstellt werden.

Sie können einen Zeiger auf eine Instanz dieser Schnittstelle abrufen, indem Sie die [**wmdrmcreateprovider**](wmdrmcreateprovider.md) -Funktion aufrufen. Zum Abrufen eines Zeigers auf eine Instanz dieser Schnittstelle, die sichere Objekte erstellen kann, müssen Sie die [**wmdrmkreateprotectedprovider**](wmdrmcreateprotectedprovider.md) -Funktion aufrufen.

## <a name="members"></a>Member

Die **iwmdrmprovider** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmdrmprovider** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmprovider** -Schnittstelle verfügt über diese Methoden.



| Methode                                              | BESCHREIBUNG                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**CreateObject**](iwmdrmprovider-createobject.md) | Ruft einen Zeiger auf eine angegebene Schnittstelle ab und erstellt bei Bedarf das implementierende Objekt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> </dl>

 

