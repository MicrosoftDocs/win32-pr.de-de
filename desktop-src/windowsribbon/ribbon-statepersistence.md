---
title: Beibehalten des Multifunktionsleisten Status
description: Das Windows Ribon-Framework (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und-Einstellungen über Anwendungs Sitzungen hinweg beizubehalten.
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a3b704151b657bdfe95845c8473a0fd197e87b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315764"
---
# <a name="persisting-ribbon-state"></a><span data-ttu-id="904bd-103">Beibehalten des Multifunktionsleisten Status</span><span class="sxs-lookup"><span data-stu-id="904bd-103">Persisting Ribbon State</span></span>

<span data-ttu-id="904bd-104">Das Windows Ribon-Framework (Menüband) bietet die Möglichkeit, den Zustand einer Vielzahl von Benutzereinstellungen und-Einstellungen über Anwendungs Sitzungen hinweg beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="904bd-104">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

-   [<span data-ttu-id="904bd-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="904bd-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="904bd-106">Vorhersagbare Darstellung</span><span class="sxs-lookup"><span data-stu-id="904bd-106">A Predictable Experience</span></span>](#a-predictable-experience)
-   [<span data-ttu-id="904bd-107">Menüband-Einstellungen speichern</span><span class="sxs-lookup"><span data-stu-id="904bd-107">Save Ribbon Settings</span></span>](#save-ribbon-settings)
-   [<span data-ttu-id="904bd-108">Menüband-Einstellungen laden</span><span class="sxs-lookup"><span data-stu-id="904bd-108">Load Ribbon Settings</span></span>](#load-ribbon-settings)
-   [<span data-ttu-id="904bd-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="904bd-109">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="904bd-110">Einführung</span><span class="sxs-lookup"><span data-stu-id="904bd-110">Introduction</span></span>

<span data-ttu-id="904bd-111">Verschiedene Aspekte eines Menübands, einschließlich der Einstellungen für Konfiguration und Interaktion, können von einem Benutzer zur Laufzeit angepasst werden, um die Benutzerfreundlichkeit und Produktivität zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="904bd-111">Various aspects of a ribbon, including configuration and interaction preferences, can be customized by a user at run time to improve usability and productivity.</span></span> <span data-ttu-id="904bd-112">Das Multifunktionsleisten-Framework stellt die Funktionalität bereit, um diese Einstellungen über mehrere Anwendungs Sitzungen hinweg durch zwei Methoden zu erhalten, die in der Implementierung der [**iuiribbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) -Schnittstelle definiert sind: [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) und [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span><span class="sxs-lookup"><span data-stu-id="904bd-112">The Ribbon framework provides the functionality to preserve these settings across application sessions through two methods defined in the implementation of the [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) interface: [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) and [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span></span>

## <a name="a-predictable-experience"></a><span data-ttu-id="904bd-113">Vorhersagbare Darstellung</span><span class="sxs-lookup"><span data-stu-id="904bd-113">A Predictable Experience</span></span>

<span data-ttu-id="904bd-114">Mit den [Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx) für die Multifunktionsleisten-Benutzer Leistung wird empfohlen, dass Multifunktionsleisten Anwendungen den Zustand des Menübands (abgesehen von der letzten ausgewählten Registerkarte) beibehalten, wenn die Anwendung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="904bd-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) advise that, to provide the most predictable user experience possible, Ribbon applications should preserve the state of the ribbon (aside from the last selected tab) as the application is closed.</span></span> <span data-ttu-id="904bd-115">Auf diese Weise können, wenn dieselbe Anwendung gestartet wird, die Einstellungen und Anpassungen aus der vorherigen Sitzung wieder hergestellt werden, und der Benutzer kann davon ausgehen, dass die Interaktion mit der Anwendung auf die gleiche Weise wie Sie verlassen wird.</span><span class="sxs-lookup"><span data-stu-id="904bd-115">In this way, when the same application is launched, the settings and customizations from the previous session can be restored and the user can expect to continue interacting with the application in the same way as they left it.</span></span>

<span data-ttu-id="904bd-116">Menü Band Einstellungen, die zur Laufzeit geändert und über Anwendungs Sitzungen hinweg beibehalten werden, werden im Kontextmenü des Befehls aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="904bd-116">Ribbon settings that can be modified at run time and preserved across application sessions are listed in the Command context menu.</span></span> <span data-ttu-id="904bd-117">Dazu gehören:</span><span class="sxs-lookup"><span data-stu-id="904bd-117">They include:</span></span>

-   <span data-ttu-id="904bd-118">Befehle, die vom Benutzer der Symbolleisten-Befehlsliste für den [schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md) hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="904bd-118">Commands added to the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) Command list by the user.</span></span> <span data-ttu-id="904bd-119">Wird von einem [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt über den [UI \_ pkey \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) -Eigenschafts Schlüssel angegeben.</span><span class="sxs-lookup"><span data-stu-id="904bd-119">Specified by an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span>

    <span data-ttu-id="904bd-120">Der folgende Screenshot zeigt den Kontextmenü Befehl **Hinzufügen zum schnell Zugriff-Symbolleiste** .</span><span class="sxs-lookup"><span data-stu-id="904bd-120">The following screen shot shows the **Add to Quick Access Toolbar** context menu Command.</span></span>

    ![Screenshot des Befehls Kontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

-   <span data-ttu-id="904bd-122">Der bevorzugte Symbolleisten-Andock Zustand des [schnell Zugriffs](windowsribbon-controls-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="904bd-122">The preferred [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) docking state.</span></span> <span data-ttu-id="904bd-123">Wird durch den [**UI- \_ controldock**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) -Wert der [UI \_ pkey \_ quickaccesstoolbardock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) -Eigenschafts Taste angegeben.</span><span class="sxs-lookup"><span data-stu-id="904bd-123">Specified by the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) value of the [UI\_PKEY\_QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) property key.</span></span>

    <span data-ttu-id="904bd-124">Dieser Screenshot zeigt die Symbolleiste für den [schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md) in der Standardposition der Titelleiste der Anwendung und die **Symbolleiste für den schnell Zugriff anzeigen unter dem** Kontextmenü Befehl des Menübands.</span><span class="sxs-lookup"><span data-stu-id="904bd-124">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) in its default application title bar location and the **Show Quick Access Toolbar below the Ribbon** context menu Command.</span></span>

    ![Screenshot des Befehls Kontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="904bd-126">Dieser Screenshot zeigt die [Symbolleiste für den schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md) unterhalb des Menübands.</span><span class="sxs-lookup"><span data-stu-id="904bd-126">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) below the ribbon.</span></span>

    ![Screenshot der Symbolleiste für den schnell Zugriff, die unter dem Menüband angedockt ist.](images/controls/qat-dockbottom.png)

-   <span data-ttu-id="904bd-128">Der von der Multifunktionsleiste minimierte Zustand, wie durch den booleschen Wert des [ \_ \_ minimierten](windowsribbon-reference-properties-uipkey-minimized.md) Eigenschafts Schlüssels der UI pkey angegeben.</span><span class="sxs-lookup"><span data-stu-id="904bd-128">The ribbon minimized state as specified by the boolean value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key.</span></span>

    > [!Note]  
    > <span data-ttu-id="904bd-129">Der minimierte Zustand des Menübands entspricht nicht dem Zustand "Multifunktionsleisten reduziert".</span><span class="sxs-lookup"><span data-stu-id="904bd-129">The ribbon minimized state is not equivalent to the ribbon collapsed state.</span></span> <span data-ttu-id="904bd-130">Im reduzierten Zustand ist das Menüband vollständig ausgeblendet und kann nicht mit interagiert werden.</span><span class="sxs-lookup"><span data-stu-id="904bd-130">When in collapsed state, the ribbon is completely hidden and cannot be interacted with.</span></span> <span data-ttu-id="904bd-131">Das Framework ruft diesen Zustand automatisch auf, wenn das Anwendungsfenster auf die Größe (horizontal oder vertikal) reduziert wird, bis zu dem Punkt, an dem die Multifunktionsleiste den Anwendungs Arbeitsbereich verdeckt.</span><span class="sxs-lookup"><span data-stu-id="904bd-131">The framework invokes this state automatically if the application window is reduced in size, either horizontally or vertically, to the point that the ribbon obscures the application workspace.</span></span> <span data-ttu-id="904bd-132">Das-Framework stellt das Menüband wieder her, wenn die Größe des Anwendungsfensters erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="904bd-132">The framework restores the ribbon when the size of the application window is increased.</span></span>

     

    <span data-ttu-id="904bd-133">Dieser Screenshot zeigt den Menübefehl "Menü **Band Kontext minimieren** ".</span><span class="sxs-lookup"><span data-stu-id="904bd-133">This screen shot shows the **Minimize the Ribbon** context menu Command.</span></span>

    ![Screenshot des Befehls Kontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="904bd-135">Dieser Screenshot zeigt eine minimierte Multifunktionsleiste.</span><span class="sxs-lookup"><span data-stu-id="904bd-135">This screen shot shows a minimized ribbon.</span></span>

    ![Screenshot des minimierten Microsoft Paint-Menübands.](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a><span data-ttu-id="904bd-137">Menüband-Einstellungen speichern</span><span class="sxs-lookup"><span data-stu-id="904bd-137">Save Ribbon Settings</span></span>

<span data-ttu-id="904bd-138">Die [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) -Methode schreibt eine binäre Darstellung des permanenten Menüband-Zustands (im vorherigen Abschnitt beschrieben) in ein [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="904bd-138">The [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method writes a binary representation of the persistent ribbon state (outlined in the previous section) to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span> <span data-ttu-id="904bd-139">Die Anwendung speichert dann den Inhalt des IStream-Objekts in einer Datei oder in der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="904bd-139">The application then saves the content of the IStream object to a file or the Windows registry.</span></span>

<span data-ttu-id="904bd-140">Im folgenden Beispiel wird der grundlegende Code veranschaulicht, der zum Schreiben des multifunktionsleistenzustands in ein [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt mithilfe der [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) -Methode erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="904bd-140">The following example demonstrates the basic code required to write the ribbon state to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span>


```C++
// pRibbon        - Pointer to the IUIRibbon interface
// ppStatusStream - Pointer to the location of a newly created IStream object
HRESULT CApplication::SaveRibbonStatusToStream(
                        __in IUIRibbon *pRibbon, 
                        __out IStream **ppStatusStream)
{
  HRESULT hr = E_FAIL; 

  *ppStatusStream = NULL;
  IStream* pStream;
  if (SUCCEEDED(hr = CreateStreamOnHGlobal(
                       NULL,  // Internally allocate a new shared memory.
                       FALSE, // Free hGlobal after IStream object released.
                       &pStream)))
  {
    if (SUCCEEDED(hr = pRibbon->SaveSettingsToStream(*ppStatusStream)))
    {                  
      pStream->AddRef();
      *ppStatusStream = pStream;
    }
    pStream->Release();
  }
  return hr;
}
```



## <a name="load-ribbon-settings"></a><span data-ttu-id="904bd-141">Menüband-Einstellungen laden</span><span class="sxs-lookup"><span data-stu-id="904bd-141">Load Ribbon Settings</span></span>

<span data-ttu-id="904bd-142">Die [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) -Methode wird verwendet, um die permanenten Informationen des Ribbon-Zustands abzurufen, die von der [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) -Methode als [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="904bd-142">The [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method is used to retrieve the persistent ribbon state information stored as an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object by the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span> <span data-ttu-id="904bd-143">Die Informationen im IStream-Objekt werden auf die Multifunktionsleisten-Benutzeroberfläche angewendet, wenn die Anwendung initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="904bd-143">The information in the IStream object is applied to the ribbon UI when the application initializes.</span></span>

<span data-ttu-id="904bd-144">Im folgenden Beispiel wird der grundlegende Code veranschaulicht, der zum Laden des Menüband-Zustands aus einem [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekt mit der [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) -Methode erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="904bd-144">The following example demonstrates the basic code required to load the ribbon state from an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object with the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>


```C++
// pRibbon       - Pointer to the IUIRibbon interface
// pStatusStream - Pointer to the IStream object that contains the Ribbon state information
HRESULT CApplication::LoadRibbonStatusFromStream(
                        __in IUIRibbon *pRibbon, 
                        __in IStream *pStatusStream)
{     
  HRESULT hr = E_FAIL;
  if (pStatusStream)
  {
    // Set the stream position to the beginning first.
    LARGE_INTEGER liStart = {0, 0};
    ULARGE_INTEGER ulActual;
    pStatusStream->Seek(liStart, STREAM_SEEK_SET, &ulActual);
    hr = pRibbon->LoadSettingsFromStream(pStatusStream);
  }
  return hr;
}
```



<span data-ttu-id="904bd-145">Um eine optimale Leistung zu erzielen, sollte die [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) -Methode während der Framework-Initialisierungsphase von der [**iuiapplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) -Rückruffunktion aufgerufen werden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="904bd-145">For optimal performance, the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method should be called from the [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) callback function during the framework initialization phase, as shown in the following example.</span></span>


```C++
IFACEMETHODIMP CMyRibbonApplication::OnViewChanged(
                                       UINT nViewID, 
                                       __in UI_VIEWTYPE typeID, 
                                       __in IUnknown* pView, 
                                       UI_VIEWVERB verb, 
                                       INT iReasonCode)
{
  HRESULT hr = E_NOTIMPL;
  if (UI_VIEWVERB_CREATE == verb)
  {
    IUIRibbon* pRibbon = NULL;
    hr = pView->QueryInterface(IID_PPV_ARGS(&pRibbon));

    if (SUCCEEDED(hr))
    {
      hr = _LoadRibbonSettings(pRibbon);
      pRibbon->Release();
    }
  }
  return hr;
}

HRESULT CMyRibbonApplication::_LoadRibbonSettings(IUIRibbon* pRibbon)
{
  ...
  pRibbon->LoadSettingsFromStream(pStream);
  ...
}
```



<span data-ttu-id="904bd-146">Mehrere Instanzen der gleichen Multifunktionsleisten-Framework-Anwendung können jeden Menüband-Zustand unabhängig als separate [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Objekte oder als Gruppe durch ein einzelnes IStream-Objekt verwalten.</span><span class="sxs-lookup"><span data-stu-id="904bd-146">Multiple instances of the same Ribbon framework application can manage each ribbon state independently as separate [IStream](/windows/win32/api/objidl/nn-objidl-istream) objects or as a group through a single IStream object.</span></span>

<span data-ttu-id="904bd-147">Beim Synchronisieren des Menüband-Zustands über eine Gruppe von Anwendungs Instanzen hinweg muss jedes Fenster der obersten Ebene auf eine [WM- \_ Aktivierungs](../inputdev/wm-activate.md) Benachrichtigung lauschen.</span><span class="sxs-lookup"><span data-stu-id="904bd-147">When synchronizing ribbon state across a group of application instances, each top-level window must listen for a [WM\_ACTIVATE](../inputdev/wm-activate.md) notification.</span></span> <span data-ttu-id="904bd-148">Das deaktivierte Fenster der obersten Ebene speichert den Multifunktionsleisten Zustand mithilfe der [**iuiribbon:: savesettingstostream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) -Methode, und das Fenster der obersten Ebene, das aktiviert wird, lädt seinen Multifunktionsleisten Zustand mithilfe der [**iuiribbon:: loadsettingsfromstream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="904bd-148">The top-level window being deactivated saves its ribbon state using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method, and the top-level window being activated loads its ribbon state using the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="904bd-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="904bd-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="904bd-150">Symbolleiste für den Schnellzugriff</span><span class="sxs-lookup"><span data-stu-id="904bd-150">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 