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
# <a name="the-getinfo-method"></a><span data-ttu-id="de922-105">Die GetInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="de922-105">The GetInfo Method</span></span>

<span data-ttu-id="de922-106">Die [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode lädt alle Attributwerte für ein ADSI-Objekt aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache.</span><span class="sxs-lookup"><span data-stu-id="de922-106">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method loads all of the attribute values for an ADSI object into the local cache from the underlying directory service.</span></span> <span data-ttu-id="de922-107">Die [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode wird verwendet, um bestimmte Attributwerte in den lokalen Cache zu laden.</span><span class="sxs-lookup"><span data-stu-id="de922-107">The [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache.</span></span> <span data-ttu-id="de922-108">Weitere Informationen zur Verwendung der **IADs:: GetInfoEx** -Methode finden Sie unter [Optimierung mit GetInfoEx](optimization-using-getinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="de922-108">For more information about using the **IADs::GetInfoEx** method, see [Optimization Using GetInfoEx](optimization-using-getinfoex.md).</span></span>

<span data-ttu-id="de922-109">ADSI führt einen impliziten [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Aufruf aus, wenn die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode oder die [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode für ein bestimmtes Attribut aufgerufen wird und kein Wert im lokalen Cache gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="de922-109">ADSI will make an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call when the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method is called for a specific attribute and no value is found in the local cache.</span></span> <span data-ttu-id="de922-110">Wenn **IADs:: GetInfo** aufgerufen wurde, wird ein impliziter Aufruf nicht wiederholt.</span><span class="sxs-lookup"><span data-stu-id="de922-110">When **IADs::GetInfo** has been called, an implicit call is not repeated.</span></span> <span data-ttu-id="de922-111">Wenn bereits ein Wert im Eigenschafts Cache vorhanden ist, wird der zwischengespeicherte Wert anstelle des aktuellen Werts aus dem zugrunde liegenden Verzeichnis abgerufen, wenn die **IADs:: Get** -Methode oder die **IADs:: Getex** -Methode aufgerufen wird, ohne dass zuerst **IADs:: GetInfo** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="de922-111">If a value already exists in the property cache, however, calling the **IADs::Get** or **IADs::GetEx** method without first calling **IADs::GetInfo** will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="de922-112">Dies kann bewirken, dass aktualisierte Attributwerte überschrieben werden, wenn der lokale Cache geändert wurde, für die Werte jedoch kein Commit in den zugrunde liegenden Verzeichnisdienst mit einem Aufrufen der [**IADs::**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="de922-112">This can cause updated attribute values to be overwritten if the local cache has been modified but the values have not been committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="de922-113">Um das Zwischenspeichern von Problemen zu vermeiden, wird der Commit-Attribut Wert durch Aufrufen von **IADs:: SetInfo** vor dem Aufrufen von **IADs:: GetInfo** geändert.</span><span class="sxs-lookup"><span data-stu-id="de922-113">To avoid caching problems, commit attribute value changes by calling **IADs::SetInfo** before calling **IADs::GetInfo**.</span></span>


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



<span data-ttu-id="de922-114">Einige Verzeichnisdienste geben nicht alle Attributwerte für ein Objekt als Reaktion auf einen [**IADs:: GetInfo-Befehl**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) zurück.</span><span class="sxs-lookup"><span data-stu-id="de922-114">Some directory services do not return all attribute values for an object in response to a [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span> <span data-ttu-id="de922-115">Verwenden Sie in diesen Fällen die [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode, um diese Werte in den lokalen Cache zu laden.</span><span class="sxs-lookup"><span data-stu-id="de922-115">In these cases, use the [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method to load these values into the local cache.</span></span>

 

 




