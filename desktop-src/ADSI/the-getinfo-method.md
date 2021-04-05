---
title: Die GetInfo-Methode
description: Die IADs-Methode "GetInfo" lädt alle Attributwerte für ein ADSI-Objekt aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- GetInfo ADSI, using IADs GetInfo
- ADSI ADSI, using, using the IADs GetInfo Method
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b374791e7fd7ff787c1b825827f410a9c15b551b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707373"
---
# <a name="the-getinfo-method"></a>Die GetInfo-Methode

Die [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode lädt alle Attributwerte für ein ADSI-Objekt aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache. Die [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode wird verwendet, um bestimmte Attributwerte in den lokalen Cache zu laden. Weitere Informationen zur Verwendung der **IADs:: GetInfoEx** -Methode finden Sie unter [Optimierung mit GetInfoEx](optimization-using-getinfoex.md).

ADSI führt einen impliziten [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Aufruf aus, wenn die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode oder die [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode für ein bestimmtes Attribut aufgerufen wird und kein Wert im lokalen Cache gefunden wird. Wenn **IADs:: GetInfo** aufgerufen wurde, wird ein impliziter Aufruf nicht wiederholt. Wenn bereits ein Wert im Eigenschafts Cache vorhanden ist, wird der zwischengespeicherte Wert anstelle des aktuellen Werts aus dem zugrunde liegenden Verzeichnis abgerufen, wenn die **IADs:: Get** -Methode oder die **IADs:: Getex** -Methode aufgerufen wird, ohne dass zuerst **IADs:: GetInfo** aufgerufen wird. Dies kann bewirken, dass aktualisierte Attributwerte überschrieben werden, wenn der lokale Cache geändert wurde, für die Werte jedoch kein Commit in den zugrunde liegenden Verzeichnisdienst mit einem Aufrufen der [**IADs::**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode ausgeführt wurde. Um das Zwischenspeichern von Problemen zu vermeiden, wird der Commit-Attribut Wert durch Aufrufen von **IADs:: SetInfo** vor dem Aufrufen von **IADs:: GetInfo** geändert.


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



Einige Verzeichnisdienste geben nicht alle Attributwerte für ein Objekt als Reaktion auf einen [**IADs:: GetInfo-Befehl**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) zurück. Verwenden Sie in diesen Fällen die [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode, um diese Werte in den lokalen Cache zu laden.

 

 




