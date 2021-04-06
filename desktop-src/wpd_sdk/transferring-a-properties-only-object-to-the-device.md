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
# <a name="transferring-a-properties-only-object-to-the-device"></a>Übertragen eines Properties-Only Objekts an das Gerät

Im Beispiel im vorherigen Thema wurde die Erstellung von Inhalten auf einem Gerät veranschaulicht, das aus Eigenschaften und Daten besteht. in diesem Thema liegt der Schwerpunkt auf der Erstellung eines reinen Eigenschafts Objekts.

Reine Eigenschaften Übertragungen werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen erreicht.



| Schnittstelle                                                          | BESCHREIBUNG                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.       |
| [**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)   | Dient zum Abrufen von Eigenschaften, die den Inhalt beschreiben. |



 

Die `TransferContactToDevice` Funktion im Modul "contenttransfer. cpp" der Beispielanwendung veranschaulicht, wie eine Anwendung Kontaktinformationen von einem PC an ein verbundenes Gerät übertragen könnte. In diesem speziellen Beispiel ist der übertragene Kontakt Name eine hart codierte "John Kane", und die übertragene Kontakt Telefonnummer lautet immer "425-555-0123".

Die erste Aufgabe, die von der- `TransferContactToDevice` Funktion ausgeführt wird, besteht darin, den Benutzer zur Eingabe eines Objekt Bezeichners für das übergeordnete Objekt auf dem Gerät aufzufordern (unter dem der Inhalt übertragen wird).


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



Der nächste Schritt ist das Abrufen von Kontakt Eigenschaften, die verwendet werden, wenn das Beispiel den neuen Kontakt auf das Gerät schreibt. Der Abruf von Kontakt Eigenschaften wird von der- `GetRequiredPropertiesForPropertiesOnlyContact` Hilfsfunktion durchgeführt.


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



Diese Funktion schreibt die folgenden Daten in ein **iportabledebug** -Objekt.

-   Der Objekt Bezeichner für das übergeordnete Element des Kontakts auf dem Gerät. (Hierbei handelt es sich um das Ziel, in dem das Gerät das Objekt speichert.)
-   Der Objekttyp (ein Kontakt).
-   Der Name des Kontakts (eine hart codierte Zeichenfolge von "John Kane").
-   Die Telefonnummer des Kontakts (eine hart codierte Zeichenfolge mit dem Wert "425-555-0123").

Im letzten Schritt wird das Eigenschaften-only-Objekt auf dem Gerät erstellt (unter Verwendung der von der-Hilfsfunktion festgelegten Eigenschaften `GetRequiredPropertiesForPropertiesOnlyContact` ). Dies wird erreicht, indem die **iportabledevicecontent:: createobjectwithpropertiesonly** -Methode aufgerufen wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



