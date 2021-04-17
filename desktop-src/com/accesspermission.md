---
title: Access spermission
description: Beschreibt die Access Control Liste (ACL) der Prinzipale, die auf Instanzen dieser Klasse zugreifen können. Diese ACL wird nur von Anwendungen verwendet, die CoInitializeSecurity nicht aufzurufen.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Access spermission-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474301"
---
# <a name="accesspermission"></a>Access spermission

Beschreibt die Access Control Liste (ACL) der Prinzipale, die auf Instanzen dieser Klasse zugreifen können. Diese ACL wird nur von Anwendungen verwendet, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg- \_ Binärwert** . Es enthält Daten, die die Access Control Liste (ACL) der Prinzipale beschreiben, die auf Instanzen dieser Klasse zugreifen können. Beim Empfang einer Anforderung zum Herstellen einer Verbindung mit einem vorhandenen Objekt dieser Klasse wird die ACL von der Anwendung geprüft, die aufgerufen wird, während die Identität des Aufrufers angenommen wird. Wenn die Zugriffs Überprüfung fehlschlägt, ist die Verbindung nicht zulässig. Wenn dieser benannte Wert nicht vorhanden ist, wird die [**DefaultAccessPermission**](defaultaccesspermission.md) -ACL getestet, um zu bestimmen, ob die Verbindung zugelassen werden muss.

Für Anwendungen, die nicht [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder nicht die [**iglobaloptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) -Schnittstelle verwenden, um die AppID anzugeben, muss die ausführbare Datei der Binärdatei der Anwendung der AppID der Anwendung zugeordnet werden, wie in [**AppID**](appid.md)beschrieben. Dies ist erforderlich, damit com die AppID der Anwendung finden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 