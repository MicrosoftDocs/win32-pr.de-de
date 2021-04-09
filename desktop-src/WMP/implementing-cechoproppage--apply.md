---
title: Implementieren von cechoproppage Apply
description: Implementieren von cechoproppage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, cechoproppage Apply-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856315"
---
# <a name="implementing-cechoproppageapply"></a><span data-ttu-id="38e8a-109">Implementieren von cechoproppage:: apply</span><span class="sxs-lookup"><span data-stu-id="38e8a-109">Implementing CEchoPropPage::Apply</span></span>

<span data-ttu-id="38e8a-110">Die cechoproppage:: Apply-Methode ist in "echoproppage. cpp" implementiert.</span><span class="sxs-lookup"><span data-stu-id="38e8a-110">The CEchoPropPage::Apply method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="38e8a-111">Sie wird ausgeführt, wenn der Benutzer im Dialogfeld Eigenschaften Seite in Windows **Media Player auf übernehmen klickt.**</span><span class="sxs-lookup"><span data-stu-id="38e8a-111">It executes when the user clicks **Apply** in the property page dialog box in Windows Media Player.</span></span> <span data-ttu-id="38e8a-112">Der Beispielcode des Plug-in-Assistenten stellt eine-Implementierung bereit, um eine einzelne Eigenschaft zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="38e8a-112">The plug-in wizard sample code provides an implementation to handle a single property.</span></span> <span data-ttu-id="38e8a-113">Sie können diesen Code für eine der Echo-Beispiel Eigenschaften ändern und dann Code hinzufügen, um den anderen Eigenschafts Wert zu speichern.</span><span class="sxs-lookup"><span data-stu-id="38e8a-113">You can modify this code for one of the Echo sample properties, and then add code to store the other property value.</span></span>

## <a name="declaring-the-apply-method-variables"></a><span data-ttu-id="38e8a-114">Deklarieren der Variablen der Apply-Methode</span><span class="sxs-lookup"><span data-stu-id="38e8a-114">Declaring the Apply Method Variables</span></span>

<span data-ttu-id="38e8a-115">Zuerst müssen Sie die Deklaration von "f" entfernen.</span><span class="sxs-lookup"><span data-stu-id="38e8a-115">First, you must remove the declaration of fScaleFactor.</span></span> <span data-ttu-id="38e8a-116">Fügen Sie dann die Variablen Deklarationen hinzu, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="38e8a-116">Then, add variable declarations that you will need.</span></span> <span data-ttu-id="38e8a-117">Das folgende Beispiel zeigt die abgeschlossenen Variablen Deklarationen:</span><span class="sxs-lookup"><span data-stu-id="38e8a-117">The following example shows the completed variable declarations:</span></span>


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a><span data-ttu-id="38e8a-118">Abrufen der Werte von der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="38e8a-118">Retrieving the Values from the Property Page</span></span>

<span data-ttu-id="38e8a-119">Sie müssen Code implementieren, um die Benutzereingabe abzurufen und zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="38e8a-119">You must implement code to retrieve and validate the user input.</span></span> <span data-ttu-id="38e8a-120">Im folgenden Codebeispiel wird der Wert für die Verzögerungszeit aus dem IDC \_ -Delta-Bearbeitungsfeld abgerufen und dann überprüft, ob der Wert innerhalb eines angegebenen Bereichs liegt:</span><span class="sxs-lookup"><span data-stu-id="38e8a-120">The following code example retrieves the delay time value from the IDC\_DELAYTIME edit box, and then verifies that the value is within a specified range:</span></span>


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



<span data-ttu-id="38e8a-121">Wenn sich die Benutzereingabe nicht im angegebenen Bereich befindet, zeigt der Code ein Meldungs Feld an.</span><span class="sxs-lookup"><span data-stu-id="38e8a-121">If the user input is not in the specified range, the code displays a message box.</span></span> <span data-ttu-id="38e8a-122">Beachten Sie die Verwendung der Zeichen folgen Ressource, die Sie zuvor für die Fehlermeldung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="38e8a-122">Notice the use of the string resource you created earlier for the error message.</span></span>

<span data-ttu-id="38e8a-123">Im folgenden Beispiel wird die Effekt Ebene aus dem Feld "IDC \_ wetmix" abgerufen und dann überprüft, ob der Wert innerhalb eines angegebenen Bereichs liegt:</span><span class="sxs-lookup"><span data-stu-id="38e8a-123">The following example retrieves the effect level from the IDC\_WETMIX edit box and then verifies that the value is within a specified range:</span></span>


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a><span data-ttu-id="38e8a-124">Speichern der Eigenschaftswerte in der Registrierung</span><span class="sxs-lookup"><span data-stu-id="38e8a-124">Storing the Property Values in the Registry</span></span>

<span data-ttu-id="38e8a-125">Als nächstes muss der Code die neuen Eigenschaftswerte in der Registrierung speichern.</span><span class="sxs-lookup"><span data-stu-id="38e8a-125">Next, your code must persist the new property values to the registry.</span></span> <span data-ttu-id="38e8a-126">Der folgende Code speichert beide Eigenschaftswerte:</span><span class="sxs-lookup"><span data-stu-id="38e8a-126">The following code stores both property values:</span></span>


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a><span data-ttu-id="38e8a-127">Aktualisieren der Eigenschaftswerte des Echo-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="38e8a-127">Updating the Echo Plug-in Property Values</span></span>

<span data-ttu-id="38e8a-128">Die **Apply** -Methode muss das Echo-Plug-in darüber informieren, dass sich die Eigenschaftswerte geändert haben.</span><span class="sxs-lookup"><span data-stu-id="38e8a-128">The **Apply** method must inform the Echo plug-in that the property values have changed.</span></span> <span data-ttu-id="38e8a-129">Der folgende Code Ruft die-Eigenschaft Put-Methode für jede Eigenschaft mit dem Schnittstellen Zeiger auf, der in cechoproppage:: SetObjects abgerufen wurde:</span><span class="sxs-lookup"><span data-stu-id="38e8a-129">The following code calls the property put method for each property using the interface pointer retrieved in CEchoPropPage::SetObjects:</span></span>


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



<span data-ttu-id="38e8a-130">Beachten Sie, dass der Wert der nass Mischung in den Gleit Komma Wert konvertiert wird, bevor er an das Plug-in übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="38e8a-130">Notice that the wet mix value is converted to floating point before being passed to the plug-in.</span></span>

## <a name="disabling-the-apply-button"></a><span data-ttu-id="38e8a-131">Deaktivieren der Schaltfläche "anwenden"</span><span class="sxs-lookup"><span data-stu-id="38e8a-131">Disabling the Apply Button</span></span>

<span data-ttu-id="38e8a-132">Im letzten Schritt sollte der Code die Apply-Eigenschaft im Dialogfeld Eigenschaften Seite als Signal an den Benutzer deaktivieren, dass die Werte erfolgreich aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="38e8a-132">As a final step, your code should disable Apply in the property page dialog box as a signal to the user that the values have been successfully updated.</span></span> <span data-ttu-id="38e8a-133">Hierfür ist die folgende einzelne Codezeile erforderlich:</span><span class="sxs-lookup"><span data-stu-id="38e8a-133">This requires the following single line of code:</span></span>


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a><span data-ttu-id="38e8a-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38e8a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38e8a-135">**Ändern der Eigenschaften Seite Echo Sample**</span><span class="sxs-lookup"><span data-stu-id="38e8a-135">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




