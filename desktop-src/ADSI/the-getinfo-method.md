---
title: Die GetInfo-Methode
description: Die GetInfo-Methode für IADs lädt alle Attributwerte für ein ADSI-Objekt aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- GetInfo ADSI mithilfe von IADs GetInfo
- ADSI ADSI mithilfe der GetInfo-Methode der IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534de8bd667ed33d562ac55b6a70452b6496d0a3d708c55a2cb0fee1a86a8a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838454"
---
# <a name="the-getinfo-method"></a>Die GetInfo-Methode

Die [**IADs::GetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) lädt alle Attributwerte für ein ADSI-Objekt aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache. Die [**IADs::GetInfoEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) wird verwendet, um bestimmte Attributwerte in den lokalen Cache zu laden. Weitere Informationen zur Verwendung der **IADs::GetInfoEx-Methode** finden Sie unter [Optimization Using GetInfoEx](optimization-using-getinfoex.md).

ADSI führt einen impliziten [**IADs::GetInfo-Aufruf**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) aus, wenn die [**IADs::Get-**](/windows/desktop/api/Iads/nf-iads-iads-get) oder [**IADs::GetEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getex) für ein bestimmtes Attribut aufgerufen wird und kein Wert im lokalen Cache gefunden wird. Wenn **IADs::GetInfo** aufgerufen wurde, wird ein impliziter Aufruf nicht wiederholt. Wenn jedoch bereits ein Wert im Eigenschaftencache vorhanden ist, ruft der Aufruf der **IADs::Get-** oder **IADs::GetEx-Methode** ohne vorherigen Aufruf von **IADs::GetInfo** den zwischengespeicherten Wert anstelle des aktuellen Werts aus dem zugrunde liegenden Verzeichnis ab. Dies kann dazu führen, dass aktualisierte Attributwerte überschrieben werden, wenn der lokale Cache geändert wurde, die Werte jedoch nicht mit einem Aufruf der [**IADs::SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) an den zugrunde liegenden Verzeichnisdienst übertragen wurden. Um Probleme beim Zwischenspeichern zu vermeiden, führen Sie einen Commit für Attributwertänderungen durch, indem **Sie IADs::SetInfo aufrufen,** bevor **Sie IADs::GetInfo aufrufen.**


```VB
Dim usr As IADs

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' This code example assumes that the property description has a single value in the directory.
' Be aware that this will IMPLICITLY call GetInfo because at this point GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's title is " + usr.Get("title")

' Change the attribute value in the local cache.
usr.Put "title", "Vice President"
Debug.Print "User's title is " + usr.Get("title")

' Call GetInfo, which will overwrite the updated value because SetInfo has not 
' been called.
usr.GetInfo
Debug.Print "User's title is " + usr.Get("title")
```



Einige Verzeichnisdienste geben nicht alle Attributwerte für ein Objekt als Antwort auf einen [**IADs::GetInfo-Aufruf**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) zurück. Verwenden Sie in diesen Fällen die [**IADs::GetInfoEx-Methode,**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) um diese Werte in den lokalen Cache zu laden.

 

 




