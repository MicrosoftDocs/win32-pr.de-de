---
description: Enthält die Methode, mit der ein Endpunkt zum Herstellen einer Verbindung mit einem Dienst verwendet wird.
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: Iupdateendpointprovider-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 81e9481f5233fac05e7fa7bdf3afa53c4c55513a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345748"
---
# <a name="iupdateendpointprovider-interface"></a>Iupdateendpointprovider-Schnittstelle

Enthält die Methode, mit der ein Endpunkt zum Herstellen einer Verbindung mit einem Dienst verwendet wird. Diese Schnittstelle wird beim Schreiben eines Endpunkt Anbieters implementiert.

## <a name="members"></a>Member

Die **iupdateendpointprovider** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iupdateendpointprovider** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iupdateendpointprovider** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**Getserviceendpoint**](iupdateendpointauthprovider-getserviceendpoint.md) | Fordert einen Endpunkt an, der zum Herstellen einer Verbindung mit einem Dienst verwendet wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

WUA Ruft die [**getserviceendpoint**](iupdateendpointauthprovider-getserviceendpoint.md) -Methode auf, um den Aushandlungs Prozess zu starten. Wenn der-Befehl durchgeführt wird, übergibt WUA die registrierten Tokentypen, und die Implementierung dieser Schnittstelle gibt die Tokentypen zurück, die verwendet werden sollen.

 

 
