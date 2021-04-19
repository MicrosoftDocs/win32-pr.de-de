---
title: Implementieren von cechoproppage OnInitDialog
description: Implementieren von cechoproppage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, cechoproppage OnInitDialog-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342042"
---
# <a name="implementing-cechoproppageoninitdialog"></a><span data-ttu-id="ac441-109">Implementieren von cechoproppage:: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="ac441-109">Implementing CEchoPropPage::OnInitDialog</span></span>

<span data-ttu-id="ac441-110">Die **cechoproppage:: OnInitDialog** -Methode ist in "echoproppage. cpp" implementiert.</span><span class="sxs-lookup"><span data-stu-id="ac441-110">The **CEchoPropPage::OnInitDialog** method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="ac441-111">Sie wird ausgeführt, wenn das Dialogfeld Eigenschaften Seite aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ac441-111">It executes when the property page dialog box is invoked.</span></span> <span data-ttu-id="ac441-112">Der Code in dieser Methode muss die aktuellen Eigenschaftswerte abrufen und im richtigen Bearbeitungsfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac441-112">The code in this method needs to retrieve the current property values and display them in the correct edit box.</span></span> <span data-ttu-id="ac441-113">Der Beispielcode des Plug-in-Assistenten stellt eine Implementierung für eine einzelne Eigenschaft bereit.</span><span class="sxs-lookup"><span data-stu-id="ac441-113">The plug-in wizard sample code provides an implementation for a single property.</span></span> <span data-ttu-id="ac441-114">Sie können diesen Code für eine der Echo-Beispiel Eigenschaften ändern und dann Code hinzufügen, um den zweiten Eigenschafts Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ac441-114">You can modify this code for one of the Echo sample properties, and then add code to retrieve the second property value.</span></span>

## <a name="declaring-the-oninitdialog-method-variables"></a><span data-ttu-id="ac441-115">Deklarieren der OnInitDialog-Methoden Variablen</span><span class="sxs-lookup"><span data-stu-id="ac441-115">Declaring the OnInitDialog Method Variables</span></span>

<span data-ttu-id="ac441-116">Zunächst müssen Sie die Deklaration von "f" entfernen und durch die folgenden Variablen Deklarationen ersetzen:</span><span class="sxs-lookup"><span data-stu-id="ac441-116">First, you must remove the declaration of fScaleFactor and replace it with the following variable declarations:</span></span>


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a><span data-ttu-id="ac441-117">Abrufen der aktuellen Werte aus dem Plug-in</span><span class="sxs-lookup"><span data-stu-id="ac441-117">Retrieving the Current Values from the Plug-in</span></span>

<span data-ttu-id="ac441-118">Der Code sollte als nächstes versuchen, die aktuellen Eigenschaftswerte aus dem Echo-Plug-in abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ac441-118">The code should next attempt to retrieve the current property values from the Echo plug-in.</span></span> <span data-ttu-id="ac441-119">Im folgenden Beispiel wird versucht, jede Eigenschaft abzurufen:</span><span class="sxs-lookup"><span data-stu-id="ac441-119">The following example attempts to retrieve each property:</span></span>


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



<span data-ttu-id="ac441-120">Im Dialogfeld wird der Wert für die Effekte-Ebene als ganze Zahl angezeigt, aber das Plug-in speichert den Wert als Gleit Komma Zahl.</span><span class="sxs-lookup"><span data-stu-id="ac441-120">The dialog box displays the effects level value to the user as an integer, but the plug-in stores the value as a floating-point number.</span></span> <span data-ttu-id="ac441-121">Daher konvertiert der Code den Gleit Komma Wert in einen **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="ac441-121">Therefore, the code converts the floating-point value to a **DWORD** value.</span></span>

## <a name="retrieving-the-current-values-from-the-registry"></a><span data-ttu-id="ac441-122">Abrufen der aktuellen Werte aus der Registrierung</span><span class="sxs-lookup"><span data-stu-id="ac441-122">Retrieving the Current Values from the Registry</span></span>

<span data-ttu-id="ac441-123">Wenn die Eigenschaften Seite die aktuellen Werte aus dem Plug-in nicht abrufen kann, muss Sie versuchen, Sie aus der Registrierung zu lesen.</span><span class="sxs-lookup"><span data-stu-id="ac441-123">If the property page cannot retrieve the current values from the plug-in, it must attempt to read them from the registry.</span></span> <span data-ttu-id="ac441-124">Der folgende Code liest die einzelnen Eigenschaftswerte:</span><span class="sxs-lookup"><span data-stu-id="ac441-124">The following code reads each property value:</span></span>


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



<span data-ttu-id="ac441-125">Beachten Sie die Verwendung der zuvor erstellten Registrierungs Konstanten.</span><span class="sxs-lookup"><span data-stu-id="ac441-125">Notice the use of the registry constants you created previously.</span></span>

## <a name="displaying-the-values-to-the-user"></a><span data-ttu-id="ac441-126">Anzeigen der Werte für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="ac441-126">Displaying the Values to the User</span></span>

<span data-ttu-id="ac441-127">Zum Schluss muss auf der Eigenschaften Seite die Werte in den richtigen Bearbeitungsfeld-Steuerelementen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ac441-127">Finally, the property page must display the values in the correct edit box controls.</span></span> <span data-ttu-id="ac441-128">Der folgende Beispielcode veranschaulicht dies:</span><span class="sxs-lookup"><span data-stu-id="ac441-128">The following example code demonstrates this:</span></span>


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a><span data-ttu-id="ac441-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac441-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac441-130">**Ändern der Eigenschaften Seite Echo Sample**</span><span class="sxs-lookup"><span data-stu-id="ac441-130">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




