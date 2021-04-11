---
title: Unterstützung für frühe Bindungen
description: Das folgende Codebeispiel zeigt ein Szenario mit einer frühen Bindungs Unterstützung.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, frühe Bindungs Unterstützung
- Binden von AD, frühe Bindungs Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102339"
---
# <a name="early-binding-support"></a><span data-ttu-id="2465d-105">Unterstützung für frühe Bindungen</span><span class="sxs-lookup"><span data-stu-id="2465d-105">Early Binding Support</span></span>

<span data-ttu-id="2465d-106">Das folgende Codebeispiel zeigt ein Szenario mit einer frühen Bindungs Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="2465d-106">The following code example presents a scenario with early binding support in place.</span></span>


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



<span data-ttu-id="2465d-107">In diesem Codebeispiel erweitern zwei Erweiterungs Komponenten ein **Benutzer** Objekt.</span><span class="sxs-lookup"><span data-stu-id="2465d-107">In this code example, two extension components extend a **user** object.</span></span> <span data-ttu-id="2465d-108">Jede Erweiterung veröffentlicht eine eigene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2465d-108">Each extension publishes its own interface.</span></span> <span data-ttu-id="2465d-109">Jede Erweiterung erkennt die andere Erweiterungsschnittstelle nicht. nur ADSI erkennt, dass beide Erweiterungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2465d-109">Each extension does not recognize the other extension interface; only ADSI recognizes the existence of both extensions.</span></span> <span data-ttu-id="2465d-110">Jede Erweiterung delegiert Ihr [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) an ADSI.</span><span class="sxs-lookup"><span data-stu-id="2465d-110">Each extension delegates its [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to ADSI.</span></span> <span data-ttu-id="2465d-111">ADSI fungiert als Aggregator für beide Erweiterungen und alle anderen zukünftigen Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="2465d-111">ADSI acts as an aggregator for both extensions, and any other future extensions.</span></span> <span data-ttu-id="2465d-112">Das Abfragen einer Schnittstelle von einer beliebigen Erweiterung oder von ADSI ergibt das gleiche konsistente Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="2465d-112">Querying an interface from any extension, or from ADSI, yields the same consistent result.</span></span>

<span data-ttu-id="2465d-113">Im folgenden Verfahren wird das Erstellen einer Erweiterung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2465d-113">The following procedure describes how to create an extension.</span></span>

## <a name="step-1-add-aggregation-to-your-component"></a><span data-ttu-id="2465d-114">Schritt 1: Hinzufügen von Aggregationen zu Ihrer Komponente</span><span class="sxs-lookup"><span data-stu-id="2465d-114">Step 1: Add Aggregation to Your Component</span></span>

<span data-ttu-id="2465d-115">Befolgen Sie die com-Spezifikation, um der Komponente Aggregationen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2465d-115">Follow the COM specification for adding aggregation to your component.</span></span> <span data-ttu-id="2465d-116">Zusammenfassend müssen Sie die *punknown* -Anforderungen Ihrer Komponente während der Erstellung von " **feateinstance**" akzeptieren und den " *punknown* " an den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) des Aggregators delegieren, wenn die Komponente aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="2465d-116">In summary, you must accept the *pUnknown* requests to your component during **CreateInstance**, and delegate the *pUnknown* to the aggregator's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) if the component is aggregated.</span></span>

## <a name="step-2-register-your-extension"></a><span data-ttu-id="2465d-117">Schritt 2: Registrieren der Erweiterung</span><span class="sxs-lookup"><span data-stu-id="2465d-117">Step 2: Register Your Extension</span></span>

<span data-ttu-id="2465d-118">Nun müssen Sie entscheiden, welche Verzeichnis Klasse erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2465d-118">Now you must decide which directory class to extend.</span></span> <span data-ttu-id="2465d-119">Sie können nicht die gleichen Schnittstellen verwenden, die Sie für eine ADSI-Schnittstelle verwenden würden, z. b. [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="2465d-119">You cannot use the same interfaces to accomplish this that you would use for an ADSI interface, for example, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span></span> <span data-ttu-id="2465d-120">Verzeichnisobjekte werden im Verzeichnis gespeichert, während ihre Erweiterung und ADSI auf dem Client Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2465d-120">Directory objects are persisted in the directory, while your extension and ADSI are running on the client computer.</span></span> <span data-ttu-id="2465d-121">Verzeichnis Objekt Beispiele sind " **User**", " **Computer**", " **PrintQueue**", " **serviceConnectionPoint**" und " **ntdsservice**".</span><span class="sxs-lookup"><span data-stu-id="2465d-121">Directory object examples are **user**, **computer**, **printQueue**, **serviceConnectionPoint**, and **nTDSService**.</span></span> <span data-ttu-id="2465d-122">Sie können in Active Directory eine neue Klasse hinzufügen und eine neue Erweiterung für diese neue Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="2465d-122">You can add a new class in Active Directory and create a new extension for this new class as well.</span></span>

<span data-ttu-id="2465d-123">Mithilfe von Registrierungs Schlüsseln ordnen Sie den ADSI-Erweiterungs Komponenten einen Verzeichnis Klassennamen zu.</span><span class="sxs-lookup"><span data-stu-id="2465d-123">You use registry keys to associate a directory class name with the ADSI extension components.</span></span> <span data-ttu-id="2465d-124">Die folgende Abbildung stellt das vorhandene Registrierungs Layout dar, sowie neue Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="2465d-124">The following figure represents the existing registry layout, as a well as new keys.</span></span>

-   <span data-ttu-id="2465d-125">Ein neuer Schlüssel namens **Erweiterungen** enthält eine Liste von Schlüsseln, von denen jeder eine Klasse im Verzeichnis darstellt.</span><span class="sxs-lookup"><span data-stu-id="2465d-125">A new key, called **Extensions**, contains a list of keys, each of which represents a class in the directory.</span></span> <span data-ttu-id="2465d-126">Jede Klasse, z. b. **Benutzer**, **PrintQueue** oder **Computer**, verwaltet eine Liste von unter Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="2465d-126">Each class, for example, **user**, **printQueue**, or **computer**, maintains a list of subkeys.</span></span>
-   <span data-ttu-id="2465d-127">Jeder Unterschlüssel enthält die CLSID der ADSI-Erweiterungs Komponente.</span><span class="sxs-lookup"><span data-stu-id="2465d-127">Each subkey contains the CLSID of the ADSI extension component.</span></span>
-   <span data-ttu-id="2465d-128">Jeder CLSID-Unterschlüssel enthält einen Zeichen folgen Eintrag, der mehrere Werte zulässt.</span><span class="sxs-lookup"><span data-stu-id="2465d-128">Each CLSID subkey contains a string entry that allows multiple values.</span></span> <span data-ttu-id="2465d-129">Sie sollten nur die Schnittstellen auflisten, die an der Aggregation beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="2465d-129">You should only list the interfaces that participate in the aggregation.</span></span>

> [!Note]  
> <span data-ttu-id="2465d-130">Erweiterungs Objekte sind weiterhin erforderlich, um Standard-com-Schlüssel zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="2465d-130">Extension objects are still required to register standard COM keys.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a><span data-ttu-id="2465d-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2465d-131">Example</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

<span data-ttu-id="2465d-132">Die Liste der Schnittstellen von Extension1 kann sich von der von Extension2 unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2465d-132">The list of interfaces from Extension1 can be different from that of Extension2.</span></span> <span data-ttu-id="2465d-133">Das-Objekt unterstützt die-Schnittstellen des Aggregators (ADSI) und alle Schnittstellen, die vom Extension1 und Extension2 des Aggregats bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2465d-133">The object, when active, supports the interfaces of the aggregator (ADSI) and all the interfaces provided by the aggregate's Extension1 and Extension2.</span></span> <span data-ttu-id="2465d-134">Auflösung von in Konflikt stehenden Schnittstellen (die gleiche Schnittstelle, die sowohl vom Aggregator als auch von Aggregaten oder mehreren Aggregaten unterstützt wird) wird durch Prioritäten der Erweiterungen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2465d-134">Resolution of conflicting interfaces (the same interface supported by both the aggregator and the aggregates or by multiple aggregates) is determined by priorities of the extensions.</span></span>

<span data-ttu-id="2465d-135">Sie können auch die CLSID-Erweiterung mehreren Objektklassen Namen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="2465d-135">You can also associate your CLSID extension with multiple object class names.</span></span> <span data-ttu-id="2465d-136">Beispielsweise kann Ihre Erweiterung sowohl das **Benutzer** -als auch das **Contact** -Objekt erweitern.</span><span class="sxs-lookup"><span data-stu-id="2465d-136">For example, your extension can extend both the **user** and **contact** objects.</span></span>

> [!Note]  
> <span data-ttu-id="2465d-137">Das Erweiterungs Verhalten wird für eine Objektklasse und nicht für eine Objektinstanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2465d-137">Extension behavior is added on a per-object class, not on a per-object instance.</span></span>

 

<span data-ttu-id="2465d-138">Als bewährte Vorgehensweise registrieren Sie Ihre Erweiterungen wie alle anderen COM-Komponenten mit einem Aufrufen der **dllregistersvr** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2465d-138">As a best practice, register your extensions, as you would any other COM components, with a call to the **DllRegisterSvr** function.</span></span> <span data-ttu-id="2465d-139">Stellen Sie außerdem eine Möglichkeit zum Aufheben der Registrierung ihrer Erweiterung bei der **DllUnregisterServer** -Funktion bereit.</span><span class="sxs-lookup"><span data-stu-id="2465d-139">Also provide a facility to unregister your extension with the **DllUnregisterServer** function.</span></span>

<span data-ttu-id="2465d-140">Im folgenden Codebeispiel wird gezeigt, wie eine-Erweiterung registriert wird.</span><span class="sxs-lookup"><span data-stu-id="2465d-140">The following code example shows how to register an extension.</span></span>


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 