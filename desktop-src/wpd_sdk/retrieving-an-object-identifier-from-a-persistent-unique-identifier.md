---
description: Abrufen eines Objekt Bezeichners aus einem persistenten eindeutigen Bezeichner
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Abrufen einer Objekt-ID aus einer permanenten eindeutigen ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368924"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a><span data-ttu-id="fdb0b-103">Abrufen einer Objekt-ID aus einer permanenten eindeutigen ID</span><span class="sxs-lookup"><span data-stu-id="fdb0b-103">Retrieving an Object Id from a Persistent Unique Id</span></span>

<span data-ttu-id="fdb0b-104">Objekt Bezeichner sind nur für eine bestimmte Geräte Sitzung eindeutig. Wenn der Benutzer eine neue Verbindung herstellt, Stimmen Bezeichner aus einer vorherigen Sitzung möglicherweise nicht mit den Bezeichners für die aktuelle Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-104">Object identifiers are only guaranteed to be unique for a given device session; if the user establishes a new connection, identifiers from a previous session may not match identifiers for the current session.</span></span> <span data-ttu-id="fdb0b-105">Um dieses Problem zu beheben, unterstützt die WPD-API persistente eindeutige Bezeichner (PUIDs), die über Geräte Sitzungen hinweg beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-105">To resolve this issue, the WPD API supports persistent unique identifiers (PUIDs), which persist across device sessions.</span></span>

<span data-ttu-id="fdb0b-106">Einige Geräte speichern Ihre PUIDs nativ mit einem bestimmten Objekt.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-106">Some devices store their PUIDs natively with a given object.</span></span> <span data-ttu-id="fdb0b-107">Andere Benutzer können die PUID basierend auf einem Hash ausgewählter Objektdaten generieren.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-107">Others may generate the PUID based on a hash of selected object data.</span></span> <span data-ttu-id="fdb0b-108">Andere können Objekt Bezeichner als PUIDs behandeln (da Sie sicherstellen können, dass diese Bezeichner niemals geändert werden).</span><span class="sxs-lookup"><span data-stu-id="fdb0b-108">Others may treat object identifiers as PUIDs (because they can guarantee that these identifiers never change).</span></span>

<span data-ttu-id="fdb0b-109">Die getobjectidentifierfrompersistentuniqueidentifier-Funktion im Modul contentproperties. cpp veranschaulicht das Abrufen eines Objekt Bezeichners für eine bestimmte PUID.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-109">The GetObjectIdentifierFromPersistentUniqueIdentifier function in the ContentProperties.cpp module demonstrates the retrieval of an object identifier for a given PUID.</span></span>

<span data-ttu-id="fdb0b-110">Die Anwendung kann einen Objekt Bezeichner für eine entsprechende PUID mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-110">Your application can retrieve an object identifier for a corresponding PUID using the interfaces described in the following table.</span></span>



| <span data-ttu-id="fdb0b-111">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fdb0b-111">Interface</span></span>                                                                                      | <span data-ttu-id="fdb0b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdb0b-112">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdb0b-113">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fdb0b-113">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="fdb0b-114">Bietet Zugriff auf die Abruf Methode.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-114">Provides access to the retrieval method.</span></span>                                                            |
| [<span data-ttu-id="fdb0b-115">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fdb0b-115">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="fdb0b-116">Wird verwendet, um den Objekt Bezeichner und den entsprechenden permanenten eindeutigen Bezeichner (PUID) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-116">Used to store both the object identifier and the corresponding persistent unique identifier (PUID).</span></span> |



 

<span data-ttu-id="fdb0b-117">Die erste Aufgabe, die von der Beispielanwendung erreicht wird, ist das Abrufen einer PUID vom Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-117">The first task that the sample application accomplishes is to obtain a PUID from the user.</span></span>


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



<span data-ttu-id="fdb0b-118">Danach ruft die Beispielanwendung ein [**iportabledevicecontent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) -Objekt ab, das verwendet wird, um die [**getobjectidsfrompersistentuniqueids**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-118">After this, the sample application retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to invoke the [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="fdb0b-119">Anschließend wird ein [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt erstellt, das die vom Benutzer bereitgestellte PUID enthält.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-119">Next, it creates an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that will hold the PUID supplied by the user.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



<span data-ttu-id="fdb0b-120">Nachdem die vorangegangenen drei Schritte ausgeführt wurden, ist das Beispiel bereit, um den Objekt Bezeichner abzurufen, der mit der vom Benutzer bereitgestellten PUID übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-120">Once the previous three steps are taken, the sample is ready to retrieve the object identifier that matches the PUID supplied by the user.</span></span> <span data-ttu-id="fdb0b-121">Dies wird erreicht, indem die [**iportabledevicecontent:: getobjectidsfrompersistentuniqueids**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-121">This is accomplished by calling the [**IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span> <span data-ttu-id="fdb0b-122">Vor dem Aufrufen dieser Methode wird im Beispiel eine PROPVARIANT-Struktur initialisiert, die vom Benutzer bereitgestellte PUID in diese Struktur geschrieben und dem iportabledevicepropvariantcollection-Objekt hinzugefügt, bei dem ppersistentuniqueids zeigt.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-122">Prior to calling this method, the sample initializes a PROPVARIANT structure, writes the PUID supplied by the user to this structure, and adds it to the IPortableDevicePropVariantCollection object at which pPersistentUniqueIDs points.</span></span> <span data-ttu-id="fdb0b-123">Dieser Zeiger wird als erstes Argument an die getobjectidsfrompersistentuniqueids-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-123">This pointer is passed as the first argument to the GetObjectIDsFromPersistentUniqueIDs method.</span></span> <span data-ttu-id="fdb0b-124">Das zweite Argument von getobjectidsfrompersistentuniqueids ist ein iportabledevicepropvariantcollection-Objekt, das den übereinstimmenden Objekt Bezeichner empfängt.</span><span class="sxs-lookup"><span data-stu-id="fdb0b-124">The second argument of GetObjectIDsFromPersistentUniqueIDs is an IPortableDevicePropVariantCollection object that receives the matching object identifier.</span></span>


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="fdb0b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fdb0b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdb0b-126">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fdb0b-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="fdb0b-127">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fdb0b-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="fdb0b-128">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fdb0b-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="fdb0b-129">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="fdb0b-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



