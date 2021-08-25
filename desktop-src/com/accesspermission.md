---
title: AccessPermission
description: Beschreibt die Access Control List (ACL) der Prinzipale, die auf Instanzen dieser Klasse zugreifen können. Diese ACL wird nur von Anwendungen verwendet, die CoInitializeSecurity nicht aufrufen.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- AccessPermission-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641512d34b963879ceb3d1a6266a017836879b224b228edb3ad62d61300fb03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551344"
---
# <a name="accesspermission"></a>AccessPermission

Beschreibt die Access Control List (ACL) der Prinzipale, die auf Instanzen dieser Klasse zugreifen können. Diese ACL wird nur von Anwendungen verwendet, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufrufen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ BINARY-Wert.** Sie enthält Daten, die die Access Control List (ACL) der Prinzipale beschreiben, die auf Instanzen dieser Klasse zugreifen können. Nach dem Empfang einer Anforderung zum Herstellen einer Verbindung mit einem vorhandenen Objekt dieser Klasse wird die ACL von der Anwendung überprüft, die aufgerufen wird, während sie die Identität des Aufrufers annimmt. Wenn bei der Zugriffsüberprüfung ein Fehler auftritt, ist die Verbindung nicht zulässig. Wenn dieser benannte Wert nicht vorhanden ist, wird die [**DefaultAccessPermission-ACL**](defaultaccesspermission.md) getestet, um zu bestimmen, ob die Verbindung zugelassen werden soll.

Für Anwendungen, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nicht aufrufen oder die [**IGlobalOptions-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) nicht verwenden, um die AppID anzugeben, muss die ausführbare Datei der Binärdatei der Anwendung der AppID der Anwendung zugeordnet werden, wie in [**AppID**](appid.md)beschrieben. Dies ist erforderlich, damit COM die AppID der Anwendung finden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 