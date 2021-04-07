---
title: Symbolleiste für den Schnellzugriff
description: Die Symbolleiste für den schnell Zugriff (QAT) ist eine kleine, anpassbare Symbolleiste, die eine Reihe von Befehlen verfügbar macht, die von der Anwendung angegeben oder vom Benutzer ausgewählt werden.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039007"
---
# <a name="quick-access-toolbar"></a><span data-ttu-id="4b159-103">Symbolleiste für den Schnellzugriff</span><span class="sxs-lookup"><span data-stu-id="4b159-103">Quick Access Toolbar</span></span>

<span data-ttu-id="4b159-104">Die Symbolleiste für den schnell Zugriff (QAT) ist eine kleine, anpassbare Symbolleiste, die eine Reihe von Befehlen verfügbar macht, die von der Anwendung angegeben oder vom Benutzer ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="4b159-104">The Quick Access Toolbar (QAT) is a small, customizable toolbar that exposes a set of Commands that are specified by the application or selected by the user.</span></span>

- [<span data-ttu-id="4b159-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="4b159-105">Introduction</span></span>](#introduction)
- [<span data-ttu-id="4b159-106">Implementieren der Symbolleiste für den schnell Zugriff</span><span class="sxs-lookup"><span data-stu-id="4b159-106">Implement the Quick Access Toolbar</span></span>](#implement-the-quick-access-toolbar)
  - [<span data-ttu-id="4b159-107">Markup</span><span class="sxs-lookup"><span data-stu-id="4b159-107">Markup</span></span>](#markup)
  - [<span data-ttu-id="4b159-108">Code</span><span class="sxs-lookup"><span data-stu-id="4b159-108">Code</span></span>](#code)
- [<span data-ttu-id="4b159-109">QAT-Persistenz</span><span class="sxs-lookup"><span data-stu-id="4b159-109">QAT Persistence</span></span>](#qat-persistence)
- [<span data-ttu-id="4b159-110">Symbolleisten Eigenschaften für den schnell Zugriff</span><span class="sxs-lookup"><span data-stu-id="4b159-110">Quick Access Toolbar Properties</span></span>](#quick-access-toolbar-properties)
- [<span data-ttu-id="4b159-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b159-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="4b159-112">Einführung</span><span class="sxs-lookup"><span data-stu-id="4b159-112">Introduction</span></span>

<span data-ttu-id="4b159-113">Standardmäßig befindet sich die Symbolleiste für den schnell Zugriff (QAT) in der Titelleiste des Anwendungsfensters, kann jedoch so konfiguriert werden, dass Sie unter dem Menüband angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4b159-113">By default, the Quick Access Toolbar (QAT) is located in the title bar of the application window but can be configured to display below the ribbon.</span></span> <span data-ttu-id="4b159-114">Neben der Bereitstellung von Befehlen enthält auch die Symbolleiste für den schnell Zugriff (QAT) ein anpassbares Dropdown Menü, das den vollständigen Satz der Standard Befehle für die schnell Zugriffs Symbolleiste (in der Symbolleiste für den schnell Zugriff) und die Menü Band Optionen enthält.</span><span class="sxs-lookup"><span data-stu-id="4b159-114">In addition to exposing Commands, the Quick Access Toolbar (QAT) also includes a customizable drop-down menu that contains the complete set of default Quick Access Toolbar (QAT) Commands (whether hidden or displayed in the Quick Access Toolbar (QAT)) and a set of Quick Access Toolbar (QAT) and ribbon options.</span></span>

<span data-ttu-id="4b159-115">Der folgende Screenshot zeigt ein Beispiel für die Symbolleiste für den schnell Zugriff auf das Menüband (QAT).</span><span class="sxs-lookup"><span data-stu-id="4b159-115">The following screen shot shows an example of the Ribbon Quick Access Toolbar (QAT).</span></span>

![Screenshot von QAT im Microsoft Paint-Menüband.](images/markup/qat-and-menu.png)

<span data-ttu-id="4b159-117">Die Symbolleiste für den schnell Zugriff (QAT) besteht aus einer Kombination aus bis zu 20 Befehlen, die entweder von der Anwendung (als "Anwendungsstandard Liste" bezeichnet) oder vom Benutzer ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="4b159-117">The Quick Access Toolbar (QAT) consists of a combination of up to 20 Commands either specified by the application (known as the application defaults list) or selected by the user.</span></span> <span data-ttu-id="4b159-118">Die Symbolleiste für den schnell Zugriff (QAT) kann eindeutige Befehle enthalten, die an anderer Stelle der Multifunktionsleisten-Benutzeroberfläche nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="4b159-118">The Quick Access Toolbar (QAT) can contain unique Commands that are not available elsewhere in the ribbon UI.</span></span>

> [!Note]
> <span data-ttu-id="4b159-119">Während fast alle multifunktionsleistensteuerelemente zulassen, dass der zugehörige Befehl der Symbolleiste für den schnell Zugriff (QAT) über das im folgenden Screenshot gezeigte Kontextmenü hinzugefügt wird, stellen Befehle, die in einem [Kontext-Popup](windowsribbon-controls-contextpopup.md) verfügbar gemacht werden, dieses Kontextmenü nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="4b159-119">While almost all ribbon controls allow their associated Command to be added to the Quick Access Toolbar (QAT) through the context menu shown in the following screen shot, Commands exposed in a [Context Popup](windowsribbon-controls-contextpopup.md) do not provide this context menu.</span></span>
>
> ![Screenshot des Befehls Kontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a><span data-ttu-id="4b159-121">Implementieren der Symbolleiste für den schnell Zugriff</span><span class="sxs-lookup"><span data-stu-id="4b159-121">Implement the Quick Access Toolbar</span></span>

<span data-ttu-id="4b159-122">Wie bei allen Windows-Menü Band Framework-Steuerelementen erfordert die vollständige Nutzung der Symbolleiste für den schnell Zugriff (QAT) sowohl eine Markup Komponente, die ihre Darstellung innerhalb des Menübands steuert, als auch eine Code Komponente, die ihre Funktionalität regelt.</span><span class="sxs-lookup"><span data-stu-id="4b159-122">As with all Windows Ribbon framework controls, taking full advantage of the Quick Access Toolbar (QAT) requires both a markup component that controls its presentation within the ribbon and a code component that governs its functionality.</span></span>

### <a name="markup"></a><span data-ttu-id="4b159-123">Markup</span><span class="sxs-lookup"><span data-stu-id="4b159-123">Markup</span></span>

<span data-ttu-id="4b159-124">Das Steuerelement für die schnell Zugriff-Symbolleiste (QAT) wurde deklariert und mit einer Befehls-ID im Markup über das [quickaccesstoolbar](windowsribbon-element-quickaccesstoolbar.md) -Element verknüpft.</span><span class="sxs-lookup"><span data-stu-id="4b159-124">The Quick Access Toolbar (QAT) control is declared, and associated with a Command ID, in markup through the [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span> <span data-ttu-id="4b159-125">Die Befehls-ID wird verwendet, um die Symbolleiste für den schnell Zugriff (QAT) an einen von der Anwendung definierten Befehls Handler zu identifizieren und zu binden.</span><span class="sxs-lookup"><span data-stu-id="4b159-125">The Command ID is used to identify and bind the Quick Access Toolbar (QAT) to a Command handler defined by the application.</span></span>

<span data-ttu-id="4b159-126">Zusätzlich zum grundlegenden Befehls Handler für die primäre Funktion für die schnell Zugriff-Symbolleiste (QAT) wird durch das Deklarieren des optionalen *customizecommandname* [quickaccesstoolbar](windowsribbon-element-quickaccesstoolbar.md) -Element Attributs der Befehlsliste im Dropdown Menü für den schnell Zugriff, für den ein sekundärer Befehls Handler definiert werden muss, ein **mehr** Befehls Element hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4b159-126">In addition to the basic Command handler for primary Quick Access Toolbar (QAT) functionality, declaring the optional *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element attribute causes the framework to add a **More Commands** item to the Command list of the Quick Access Toolbar (QAT) drop-down menu that requires a secondary Command handler be defined.</span></span>

<span data-ttu-id="4b159-127">Um Konsistenz zwischen Multifunktionsleisten-Anwendungen zu gewährleisten, wird empfohlen, dass der *customizecommandname* -Befehls Handler das Anpassungs Dialogfeld für den schnell Zugriff (QAT) startet.</span><span class="sxs-lookup"><span data-stu-id="4b159-127">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a Quick Access Toolbar (QAT) customization dialog.</span></span> <span data-ttu-id="4b159-128">Da das Multifunktionsleisten Framework nur den Ausgangspunkt in der Benutzeroberfläche bereitstellt, ist die Anwendung allein dafür verantwortlich, die Anpassungs dialogdialogfeld-Implementierung bereitzustellen, wenn die Rückruf Benachrichtigung für diesen Befehl empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="4b159-128">Because the Ribbon framework only provides the launching point in the UI, the application is solely responsible for providing the customization dialog implementation when the callback notification for this Command is received.</span></span>

<span data-ttu-id="4b159-129">Der folgende Screenshot zeigt das Dropdown Menü für den schnell Zugriff-Symbolleiste (QAT) mit dem Befehls Element **Weitere Befehle** .</span><span class="sxs-lookup"><span data-stu-id="4b159-129">The following screen shot shows a Quick Access Toolbar (QAT) drop-down menu with the **More Commands** Command item.</span></span>

![Screenshot eines QAT-Menüs mit den weiteren Befehlen... Befehls Element.](images/markup/qat-customizecommandname.png)

<span data-ttu-id="4b159-131">Die Liste mit den Anwendungs Standardwerten für die Symbolleiste für den schnell Zugriff (QAT) wird über die [quickaccesstoolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) -Eigenschaft angegeben, die eine Standardliste empfohlener Befehle identifiziert, die alle im Dropdown Menü schnell Zugriff-Symbolleiste (QAT) aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="4b159-131">The application defaults list for the Quick Access Toolbar (QAT) is specified through the [QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) property which identifies a default list of recommended Commands, all of which are listed in the Quick Access Toolbar (QAT) drop-down menu.</span></span>

<span data-ttu-id="4b159-132">Zum Anzeigen von Befehlen aus der Liste Anwendungs Standardwerte auf der Symbolleiste für die schnell Zugriffs Symbolleiste (QAT) muss das *ApplicationDefaults. IsChecked* -Attribut jedes Steuer Elements den Wert aufweisen `true` .</span><span class="sxs-lookup"><span data-stu-id="4b159-132">To display Commands from the application defaults list in the Quick Access Toolbar (QAT) toolbar, the *ApplicationDefaults.IsChecked* attribute of each control element must have a value of `true`.</span></span> <span data-ttu-id="4b159-133">In den vorangehenden Bildern werden die Ergebnisse der Einstellung dieses Attributs auf `true` für die Befehle zum **Speichern**, Rückgängigmachen und wieder **holen** angezeigt. </span><span class="sxs-lookup"><span data-stu-id="4b159-133">The preceding images show the results of setting this attribute to `true` for the **Save**, **Undo**, and **Redo** Commands.</span></span>

<span data-ttu-id="4b159-134">[Quickaccesstoolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) unterstützt drei Typen von Menü Band Steuerelementen: [Schalt](windowsribbon-controls-button.md)Fläche, [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md)und [Kontrollkästchen](windowsribbon-controls-checkbox.md).</span><span class="sxs-lookup"><span data-stu-id="4b159-134">[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supports three types of Ribbon controls: [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), and [Check Box](windowsribbon-controls-checkbox.md).</span></span>

> [!Note]
> <span data-ttu-id="4b159-135">Windows 8 und höher: alle Katalog basierten Steuerelemente werden unterstützt ([ComboBox](windowsribbon-element-combobox.md), [inribbongallery](windowsribbon-element-inribbongallery.md), [splitbuttongallery](windowsribbon-element-splitbuttongallery.md)und [dropdowngallery](windowsribbon-element-dropdowngallery.md)).</span><span class="sxs-lookup"><span data-stu-id="4b159-135">Windows 8 and newer: All gallery-based controls are supported ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md), and [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span></span>
>
> <span data-ttu-id="4b159-136">Elemente in einem Katalog-Steuerelement können Hervorhebung bei Hover unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4b159-136">Items in a gallery control can support highlighting on hover.</span></span> <span data-ttu-id="4b159-137">Zur Unterstützung der Hover-Hervorhebung muss der Katalog ein Element Katalog sein und ein [flowmenulayout](windowsribbon-element-flowmenulayout.md) des Typs [verticalmenulayout](windowsribbon-element-verticalmenulayout.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b159-137">To support hover highlighting, the gallery must be an items gallery and use a [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) of type [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span></span>

<span data-ttu-id="4b159-138">Im folgenden Beispiel wird das grundlegende Markup für ein [quickaccesstoolbar](windowsribbon-element-quickaccesstoolbar.md) -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4b159-138">The following example demonstrates the basic markup for a [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

<span data-ttu-id="4b159-139">In diesem Code Abschnitt werden die Befehls Deklarationen für ein Element für die [schnell Zugriffs Symbolleiste (QAT)](windowsribbon-element-quickaccesstoolbar.md) gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b159-139">This section of code shows the Command declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

<span data-ttu-id="4b159-140">Dieser Code Abschnitt zeigt die Steuerelement Deklarationen für ein Element für die [schnell Zugriffs Symbolleiste (QAT)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="4b159-140">This section of code shows the control declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```

### <a name="code"></a><span data-ttu-id="4b159-141">Code</span><span class="sxs-lookup"><span data-stu-id="4b159-141">Code</span></span>

<span data-ttu-id="4b159-142">Die Menüband-Framework-Anwendung muss eine Befehls Handler-Rückruf Methode bereitstellen, um die Symbolleiste für den schnell Zugriff zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4b159-142">The Ribbon framework application must provide a Command handler callback method to manipulate the Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="4b159-143">Dieser Handler funktioniert ähnlich wie Befehls Katalog Handler, mit der Ausnahme, dass die Symbolleiste für den schnell Zugriff (QAT) keine Kategorien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b159-143">This handler works in a similar fashion to Command gallery handlers, except that the Quick Access Toolbar (QAT) does not support categories.</span></span> <span data-ttu-id="4b159-144">Weitere Informationen finden Sie unter [Arbeiten mit Galerien](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="4b159-144">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="4b159-145">Die Befehls Auflistung für die schnell Zugriff-Symbolleiste (QAT) wird als [iuicollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt über den [UI \_ pkey \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) -Eigenschafts Schlüssel abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4b159-145">The Quick Access Toolbar (QAT) Command collection is retrieved as an [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span> <span data-ttu-id="4b159-146">Sie können der Symbolleiste für den schnell Zugriff (QAT) zur Laufzeit Befehle hinzufügen, indem Sie der **iuicollection** ein [iuisimplepropertyset](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4b159-146">Adding Commands to the Quick Access Toolbar (QAT) at run time is accomplished by adding an [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object to the **IUICollection**.</span></span>

<span data-ttu-id="4b159-147">Im Unterschied zu Befehls Galerien ist eine Eigenschaft des Befehls Typs ([UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) für das [iuisimplepropertyset](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt der schnell Zugriffs Symbolleiste (QAT) nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b159-147">Unlike Command galleries, a command type property ([UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) is not required for the Quick Access Toolbar (QAT) [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object.</span></span> <span data-ttu-id="4b159-148">Allerdings muss der Befehl im Menüband oder in der Symbolleiste für die schnell Zugriffs Symbolleiste (QAT) mit der Standardliste der Anwendungen ein neuer Befehl kann nicht zur Laufzeit erstellt und der Symbolleiste für den schnell Zugriff hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4b159-148">However, the Command must exist in the ribbon or Quick Access Toolbar (QAT) application defaults list; a new Command cannot be created at run time and added to the Quick Access Toolbar (QAT).</span></span>

> [!Note]  
> <span data-ttu-id="4b159-149">Die Menüband-Anwendung kann die [iuicollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) für den schnell Zugriff (QAT) nicht durch ein benutzerdefiniertes Sammlungsobjekt ersetzen, das von IEnumUnknown abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="4b159-149">The Ribbon application cannot replace the Quick Access Toolbar (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) with a custom collection object derived from IEnumUnknown.</span></span>

<span data-ttu-id="4b159-150">Das folgende Beispiel veranschaulicht eine einfache Implementierung des Befehls Handlers für die schnell Zugriffs Symbolleiste (QAT).</span><span class="sxs-lookup"><span data-stu-id="4b159-150">The following example demonstrates a basic Quick Access Toolbar (QAT) Command handler implementation.</span></span>

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a><span data-ttu-id="4b159-151">QAT-Persistenz</span><span class="sxs-lookup"><span data-stu-id="4b159-151">QAT Persistence</span></span>

<span data-ttu-id="4b159-152">Die Befehls Elemente und-Einstellungen für die schnell Zugriffs Symbolleiste (QAT) können über Anwendungs Sitzungen hinweg beibehalten werden, indem die Funktionen " [iuiribbon:: savesettingstostream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) " und " [iuiribbon:: loadsettingsfromstream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) " verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b159-152">Quick Access Toolbar (QAT) Command items and settings can be persisted across application sessions using the [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) and [IUIRibbon::LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) functions.</span></span> <span data-ttu-id="4b159-153">Weitere Informationen finden Sie unter [persistenzstatus der Multifunktionsleiste](ribbon-statepersistence.md).</span><span class="sxs-lookup"><span data-stu-id="4b159-153">For more information, see [Persisting Ribbon State](ribbon-statepersistence.md).</span></span>

## <a name="quick-access-toolbar-properties"></a><span data-ttu-id="4b159-154">Symbolleisten Eigenschaften für den schnell Zugriff</span><span class="sxs-lookup"><span data-stu-id="4b159-154">Quick Access Toolbar Properties</span></span>

<span data-ttu-id="4b159-155">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Steuerelement für die schnell Zugriffs Symbolleiste (QAT).</span><span class="sxs-lookup"><span data-stu-id="4b159-155">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Quick Access Toolbar (QAT) control.</span></span>

<span data-ttu-id="4b159-156">In der Regel wird eine Eigenschaft für die schnell Zugriffs Symbolleiste (QAT) in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Aufrufen der [iuiframework:: invalidateuicommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="4b159-156">Typically, a Quick Access Toolbar (QAT) property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [IUIFramework::InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="4b159-157">Das Invalidierung-Ereignis wird durch die [iuicommandhandler:: updateproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="4b159-157">The invalidation event is handled, and the property updates defined, by the [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="4b159-158">Die [iuicommandhandler:: updateproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="4b159-158">The [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="4b159-159">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4b159-159">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="4b159-160">In einigen Fällen kann eine Eigenschaft durch die [iuiframework:: getuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [iuiframework:: setuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4b159-160">In some cases, a property can be retrieved through the [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

<span data-ttu-id="4b159-161">In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die mit dem Steuerelement für die schnell Zugriffs Symbolleiste (QAT) verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="4b159-161">The following table lists the property keys that are associated with the Quick Access Toolbar (QAT) control.</span></span>

| <span data-ttu-id="4b159-162">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="4b159-162">Property Key</span></span> | <span data-ttu-id="4b159-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b159-163">Notes</span></span> |
|---|---|
| [<span data-ttu-id="4b159-164">UI- \_ pkey \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="4b159-164">UI\_PKEY\_ItemsSource</span></span>](windowsribbon-reference-properties-uipkey-itemssource.md) | <span data-ttu-id="4b159-165">Unterstützt [iuiframework:: getuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (bietet keine Unterstützung für [iuiframework:: mintuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [Iuiframework:: getuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) gibt einen Zeiger auf ein iuicollection-Objekt zurück, das die Befehle in der QAT darstellt.</span><span class="sxs-lookup"><span data-stu-id="4b159-165">Supports [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (does not support [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)).[IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) returns a pointer to an IUICollection object that represents the commands in the QAT.</span></span> <span data-ttu-id="4b159-166">Jeder Befehl wird durch die Befehls-ID identifiziert, die durch Aufrufen der [iuisimplepropertyset:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) -Methode abgerufen wird, und übergibt den Eigenschafts Schlüssel [UI \_ pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md).</span><span class="sxs-lookup"><span data-stu-id="4b159-166">Each Command is identified by its Command ID, which is obtained by calling the [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method and passing in the property key [UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md).</span></span> |

<span data-ttu-id="4b159-167">Dem Befehls Element " **Weitere Befehle** " im Dropdown Menü "schnell Zugriff" (QAT) sind keine Eigenschafts Schlüssel zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4b159-167">There are no property keys associated with the **More Commands** Command item of the Quick Access Toolbar (QAT) drop-down menu</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b159-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b159-168">Related topics</span></span>

- [<span data-ttu-id="4b159-169">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b159-169">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
- [<span data-ttu-id="4b159-170">Quickaccesstoolbar-Markup Element</span><span class="sxs-lookup"><span data-stu-id="4b159-170">QuickAccessToolbar markup element</span></span>](windowsribbon-element-quickaccesstoolbar.md)