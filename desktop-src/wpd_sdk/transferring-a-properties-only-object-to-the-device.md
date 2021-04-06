---
description: Übertragen eines Properties-Only Objekts an das Gerät
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: Übertragen eines Properties-Only Objekts an das Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758449"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a><span data-ttu-id="26e99-103">Übertragen eines Properties-Only Objekts an das Gerät</span><span class="sxs-lookup"><span data-stu-id="26e99-103">Transferring a Properties-Only Object to the Device</span></span>

<span data-ttu-id="26e99-104">Im Beispiel im vorherigen Thema wurde die Erstellung von Inhalten auf einem Gerät veranschaulicht, das aus Eigenschaften und Daten besteht. in diesem Thema liegt der Schwerpunkt auf der Erstellung eines reinen Eigenschafts Objekts.</span><span class="sxs-lookup"><span data-stu-id="26e99-104">While the example in the previous topic demonstrated the creation of content on a device consisting of both properties and data, this topic focuses on the creation of a properties-only object.</span></span>

<span data-ttu-id="26e99-105">Reine Eigenschaften Übertragungen werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen erreicht.</span><span class="sxs-lookup"><span data-stu-id="26e99-105">Property-only transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="26e99-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="26e99-106">Interface</span></span>                                                          | <span data-ttu-id="26e99-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26e99-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="26e99-108">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="26e99-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | <span data-ttu-id="26e99-109">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="26e99-109">Provides access to the content-specific methods.</span></span>       |
| [<span data-ttu-id="26e99-110">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="26e99-110">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)   | <span data-ttu-id="26e99-111">Dient zum Abrufen von Eigenschaften, die den Inhalt beschreiben.</span><span class="sxs-lookup"><span data-stu-id="26e99-111">Used to retrieve properties that describe the content.</span></span> |



 

<span data-ttu-id="26e99-112">Die `TransferContactToDevice` Funktion im Modul "contenttransfer. cpp" der Beispielanwendung veranschaulicht, wie eine Anwendung Kontaktinformationen von einem PC an ein verbundenes Gerät übertragen könnte.</span><span class="sxs-lookup"><span data-stu-id="26e99-112">The `TransferContactToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a PC to a connected device.</span></span> <span data-ttu-id="26e99-113">In diesem speziellen Beispiel ist der übertragene Kontakt Name eine hart codierte "John Kane", und die übertragene Kontakt Telefonnummer lautet immer "425-555-0123".</span><span class="sxs-lookup"><span data-stu-id="26e99-113">In this particular sample, the transferred contact name is a hard-coded "John Kane" and the transferred contact phone number is always "425-555-0123".</span></span>

<span data-ttu-id="26e99-114">Die erste Aufgabe, die von der- `TransferContactToDevice` Funktion ausgeführt wird, besteht darin, den Benutzer zur Eingabe eines Objekt Bezeichners für das übergeordnete Objekt auf dem Gerät aufzufordern (unter dem der Inhalt übertragen wird).</span><span class="sxs-lookup"><span data-stu-id="26e99-114">The first task accomplished by the `TransferContactToDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="26e99-115">Der nächste Schritt ist das Abrufen von Kontakt Eigenschaften, die verwendet werden, wenn das Beispiel den neuen Kontakt auf das Gerät schreibt.</span><span class="sxs-lookup"><span data-stu-id="26e99-115">The next step is the retrieval of contact properties, which will be used when the sample writes the new contact to the device.</span></span> <span data-ttu-id="26e99-116">Der Abruf von Kontakt Eigenschaften wird von der- `GetRequiredPropertiesForPropertiesOnlyContact` Hilfsfunktion durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="26e99-116">The retrieval of contact properties is performed by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function.</span></span>


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="26e99-117">Diese Funktion schreibt die folgenden Daten in ein **iportabledebug** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="26e99-117">This function writes the following data to an **IPortableDeviceValues** object.</span></span>

-   <span data-ttu-id="26e99-118">Der Objekt Bezeichner für das übergeordnete Element des Kontakts auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="26e99-118">The object identifier for the contact's parent on the device.</span></span> <span data-ttu-id="26e99-119">(Hierbei handelt es sich um das Ziel, in dem das Gerät das Objekt speichert.)</span><span class="sxs-lookup"><span data-stu-id="26e99-119">(This is the destination where the device will store the object.)</span></span>
-   <span data-ttu-id="26e99-120">Der Objekttyp (ein Kontakt).</span><span class="sxs-lookup"><span data-stu-id="26e99-120">The object type (a contact).</span></span>
-   <span data-ttu-id="26e99-121">Der Name des Kontakts (eine hart codierte Zeichenfolge von "John Kane").</span><span class="sxs-lookup"><span data-stu-id="26e99-121">The contact name (a hard coded string of "John Kane").</span></span>
-   <span data-ttu-id="26e99-122">Die Telefonnummer des Kontakts (eine hart codierte Zeichenfolge mit dem Wert "425-555-0123").</span><span class="sxs-lookup"><span data-stu-id="26e99-122">The contact phone number (a hard-coded string of "425-555-0123").</span></span>

<span data-ttu-id="26e99-123">Im letzten Schritt wird das Eigenschaften-only-Objekt auf dem Gerät erstellt (unter Verwendung der von der-Hilfsfunktion festgelegten Eigenschaften `GetRequiredPropertiesForPropertiesOnlyContact` ).</span><span class="sxs-lookup"><span data-stu-id="26e99-123">The final step creates the properties-only object on the device (using the properties set by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function).</span></span> <span data-ttu-id="26e99-124">Dies wird erreicht, indem die **iportabledevicecontent:: createobjectwithpropertiesonly** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="26e99-124">This is accomplished by calling the **IPortableDeviceContent::CreateObjectWithPropertiesOnly** method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
}
```



## <a name="related-topics"></a><span data-ttu-id="26e99-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26e99-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26e99-126">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="26e99-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="26e99-127">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="26e99-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="26e99-128">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="26e99-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="26e99-129">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="26e99-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



