---
description: Enthält die Methoden, die zum Aushandeln der Art des Tokens verwendet werden, das zum Authentifizieren des Endpunkts eines Diensts verwendet wird.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Iupdateendpointauthprovider-Schnittstelle (updateendpointauth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526684"
---
# <a name="iupdateendpointauthprovider-interface"></a>Iupdateendpointauthprovider-Schnittstelle

Die **iupdateendpointauthprovider** -Schnittstelle enthält die Methoden, die zum Aushandeln des Tokentyps verwendet werden, der zum Authentifizieren des Endpunkts eines Diensts verwendet wird.

## <a name="members"></a>Member

Die **iupdateendpointauthprovider** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iupdateendpointauthprovider** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iupdateendpointauthprovider** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                             | BESCHREIBUNG                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Getendpointtoken**](iupdateendpointauthprovider-getendpointtoken.md)                           | Fordern Sie ein Token für den Endpunkt des Diensts mit den angegebenen Anmelde Informationen an.<br/>    |
| [**Getpreferredendpointpokentype**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | Gibt den bevorzugten Authentifizierungstyp für den Endpunkt des Diensts zurück.<br/> |



 

## <a name="remarks"></a>Bemerkungen

WUA Ruft die [**getpreferredendpointdekentype**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) -Methode dieser Schnittstelle auf, um den Aushandlungs Prozess zu starten. Wenn der-Befehl durchgeführt wird, übergibt WUA den Dienst Bezeichner, den Typ des Endpunkts, der vom Dienst implementiert wird, und die verfügbaren Tokentypen. Die Implementierung dieser Schnittstelle gibt dann die Tokentypen zurück, die für die Verwendung bevorzugt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>Updateendpointauth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Updateendpointauth. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Updateendpointauth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
