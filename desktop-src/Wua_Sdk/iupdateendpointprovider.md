---
description: Enthält die Methode zum Abrufen eines Endpunkts, der zum Herstellen einer Verbindung mit einem Dienst verwendet wird.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: IUpdateEndpointProvider-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 2242e30ccd64c0252d5a1ea97eedd865f9e80bee2c58f749ca6d2eabd64c6167
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896840"
---
# <a name="iupdateendpointprovider-interface"></a>IUpdateEndpointProvider-Schnittstelle

Enthält die Methode zum Abrufen eines Endpunkts, der zum Herstellen einer Verbindung mit einem Dienst verwendet wird. Diese Schnittstelle wird beim Schreiben eines Endpunktanbieters implementiert.

## <a name="members"></a>Member

Die **IUpdateEndpointProvider-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointProvider** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IUpdateEndpointProvider-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) | Fordert einen Endpunkt an, der zum Herstellen einer Verbindung mit einem Dienst verwendet wird.<br/> |



 

## <a name="remarks"></a>Hinweise

WUA ruft die [**GetServiceEndpoint-Methode**](iupdateendpointauthprovider-getserviceendpoint.md) auf, um den Aushandlungsprozess zu starten. Wenn der Aufruf erfolgt, übergibt WUA die registrierten Tokentypen, und die Implementierung dieser Schnittstelle gibt die Tokentypen zurück, die er bevorzugt verwendet.

 

 
