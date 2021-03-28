---
description: Ein Großteil der Implementierung eines Shellerweiterungs-Handlerobjekts wird durch seinen Typ vorgegeben. Es gibt jedoch einige allgemeine Elemente. In diesem Thema werden die Aspekte der Implementierung erläutert, die von allen Shellerweiterungs Handlern gemeinsam genutzt werden.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Initialisieren von Shellerweiterungs Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980777"
---
# <a name="initializing-shell-extension-handlers"></a><span data-ttu-id="088ef-105">Initialisieren von Shellerweiterungs Handlern</span><span class="sxs-lookup"><span data-stu-id="088ef-105">Initializing Shell Extension Handlers</span></span>

<span data-ttu-id="088ef-106">Ein Großteil der Implementierung eines Shellerweiterungs-Handlerobjekts wird durch seinen Typ vorgegeben.</span><span class="sxs-lookup"><span data-stu-id="088ef-106">Much of the implementation of a Shell extension handler object is dictated by its type.</span></span> <span data-ttu-id="088ef-107">Es gibt jedoch einige allgemeine Elemente.</span><span class="sxs-lookup"><span data-stu-id="088ef-107">There are, however, some common elements.</span></span> <span data-ttu-id="088ef-108">In diesem Thema werden die Aspekte der Implementierung erläutert, die von allen Shellerweiterungs Handlern gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="088ef-108">This topic discusses those aspects of implementation that are shared by all Shell extension handlers.</span></span>

<span data-ttu-id="088ef-109">Alle Shellerweiterungs Handler sind in-Process-Component Object Model (com)-Objekten.</span><span class="sxs-lookup"><span data-stu-id="088ef-109">All Shell extension handlers are in-process Component Object Model (COM) objects.</span></span> <span data-ttu-id="088ef-110">Sie müssen eine GUID zugewiesen und wie unter [Registrieren von Shellerweiterungs Handlern](handlers.md)beschrieben registriert sein.</span><span class="sxs-lookup"><span data-stu-id="088ef-110">They must be assigned a GUID and registered as described in [Registering Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="088ef-111">Sie werden als DLLs implementiert und müssen die folgenden Standardfunktionen exportieren:</span><span class="sxs-lookup"><span data-stu-id="088ef-111">They are implemented as DLLs and must export the following standard functions:</span></span>

-   <span data-ttu-id="088ef-112">[**DllMain**](../dlls/dllmain.md).</span><span class="sxs-lookup"><span data-stu-id="088ef-112">[**DllMain**](../dlls/dllmain.md).</span></span> <span data-ttu-id="088ef-113">Der Standard Einstiegspunkt für die dll.</span><span class="sxs-lookup"><span data-stu-id="088ef-113">The standard entry point to the DLL.</span></span>
-   <span data-ttu-id="088ef-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span><span class="sxs-lookup"><span data-stu-id="088ef-114">[**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject).</span></span> <span data-ttu-id="088ef-115">Macht die Klassenfactory des Objekts verfügbar.</span><span class="sxs-lookup"><span data-stu-id="088ef-115">Exposes the object's class factory.</span></span>
-   <span data-ttu-id="088ef-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span><span class="sxs-lookup"><span data-stu-id="088ef-116">[**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow).</span></span> <span data-ttu-id="088ef-117">COM ruft diese Funktion auf, um zu bestimmen, ob das Objekt Clients bedient.</span><span class="sxs-lookup"><span data-stu-id="088ef-117">COM calls this function to determine whether the object is serving any clients.</span></span> <span data-ttu-id="088ef-118">Andernfalls kann das System die DLL entladen und den zugeordneten Speicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="088ef-118">If not, the system can unload the DLL and free the associated memory.</span></span>

<span data-ttu-id="088ef-119">Wie alle COM-Objekte müssen Shellerweiterungs Handler eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle und eine [Klassenfactory](../com/implementing-iclassfactory.md)implementieren.</span><span class="sxs-lookup"><span data-stu-id="088ef-119">Like all COM objects, Shell extension handlers must implement an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a [class factory](../com/implementing-iclassfactory.md).</span></span> <span data-ttu-id="088ef-120">In den meisten Fällen muss in Windows XP oder früher entweder eine [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -oder [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="088ef-120">Most must also implement either an [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface in Windows XP or earlier.</span></span> <span data-ttu-id="088ef-121">Diese wurden durch [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) und [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista ersetzt.</span><span class="sxs-lookup"><span data-stu-id="088ef-121">These were replaced by [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) and [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) in Windows Vista.</span></span> <span data-ttu-id="088ef-122">Die Shell verwendet diese Schnittstellen, um den Handler zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="088ef-122">The Shell uses these interfaces to initialize the handler.</span></span>

<span data-ttu-id="088ef-123">Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle muss folgendermaßen implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="088ef-123">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="088ef-124">Symbol Handler</span><span class="sxs-lookup"><span data-stu-id="088ef-124">Icon handlers</span></span>
-   <span data-ttu-id="088ef-125">Daten Handler</span><span class="sxs-lookup"><span data-stu-id="088ef-125">Data handlers</span></span>
-   <span data-ttu-id="088ef-126">Drop Handler</span><span class="sxs-lookup"><span data-stu-id="088ef-126">Drop handlers</span></span>

<span data-ttu-id="088ef-127">Die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle muss wie folgt implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="088ef-127">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface must be implemented by the following:</span></span>

-   <span data-ttu-id="088ef-128">Handler für Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="088ef-128">Shortcut menu handlers</span></span>
-   <span data-ttu-id="088ef-129">Drag & Drop-Handler</span><span class="sxs-lookup"><span data-stu-id="088ef-129">Drag-and-drop handlers</span></span>
-   <span data-ttu-id="088ef-130">Eigenschaften Blatt Handler</span><span class="sxs-lookup"><span data-stu-id="088ef-130">Property sheet handlers</span></span>

<span data-ttu-id="088ef-131">Im restlichen Teil dieses Themas werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="088ef-131">The following subjects are discussed in the remainder of this topic:</span></span>

-   [<span data-ttu-id="088ef-132">Implementieren von IPersistFile</span><span class="sxs-lookup"><span data-stu-id="088ef-132">Implementing IPersistFile</span></span>](#implementing-ipersistfile)
-   [<span data-ttu-id="088ef-133">Implementieren von ishellextinit</span><span class="sxs-lookup"><span data-stu-id="088ef-133">Implementing IShellExtInit</span></span>](#implementing-ishellextinit)
-   [<span data-ttu-id="088ef-134">Infotip-Anpassung</span><span class="sxs-lookup"><span data-stu-id="088ef-134">Infotip Customization</span></span>](#infotip-customization)
-   [<span data-ttu-id="088ef-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="088ef-135">Related topics</span></span>](#related-topics)

## <a name="implementing-ipersistfile"></a><span data-ttu-id="088ef-136">Implementieren von IPersistFile</span><span class="sxs-lookup"><span data-stu-id="088ef-136">Implementing IPersistFile</span></span>

<span data-ttu-id="088ef-137">Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle ist so konzipiert, dass ein Objekt aus einer Datenträger Datei geladen oder in einer Datei gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="088ef-137">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is designed to permit an object to be loaded from or saved to a disk file.</span></span> <span data-ttu-id="088ef-138">Sie verfügt über sechs Methoden, zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), fünf ihrer eigenen und der [**GetClassID-**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) Methode, die von [**ipersistent**](/windows/win32/api/objidl/nn-objidl-ipersist)erbt.</span><span class="sxs-lookup"><span data-stu-id="088ef-138">It has six methods in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), five of its own, and the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) method that it inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist).</span></span> <span data-ttu-id="088ef-139">Bei Shellerweiterungen wird **ipersistent** nur zum Initialisieren eines Shellerweiterungs-Handlerobjekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="088ef-139">With Shell extensions, **IPersist** is used only to initialize a Shell extension handler object.</span></span> <span data-ttu-id="088ef-140">Da in der Regel kein Lese-oder Schreibzugriff auf den Datenträger erforderlich ist, benötigen nur die Methoden **GetClassID** und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) eine nicht Token-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="088ef-140">Because there is typically no need to read from or write to the disk, only the **GetClassID** and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods require a nontoken implementation.</span></span>

<span data-ttu-id="088ef-141">Die Shell ruft zuerst [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) auf, und die-Funktion gibt den Klassen Bezeichner (CLSID) des Erweiterungs Handler-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="088ef-141">The Shell calls [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) first, and the function returns the class identifier (CLSID) of the extension handler object.</span></span> <span data-ttu-id="088ef-142">Die Shell ruft dann [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) auf und übergibt zwei Werte.</span><span class="sxs-lookup"><span data-stu-id="088ef-142">The Shell then calls [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) and passes in two values.</span></span> <span data-ttu-id="088ef-143">Der erste *pszFile-Datentyp* ist eine Unicode-Zeichenfolge mit dem Namen der Datei oder des Ordners, mit der die Shell arbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="088ef-143">The first, *pszFile*, is a Unicode string with the name of the file or folder that Shell is about to operate on.</span></span> <span data-ttu-id="088ef-144">Die zweite ist der *dwmode*, der den Datei Zugriffsmodus angibt.</span><span class="sxs-lookup"><span data-stu-id="088ef-144">The second is *dwMode*, which indicates the file access mode.</span></span> <span data-ttu-id="088ef-145">Da der Zugriff auf Dateien normalerweise nicht erforderlich ist, ist *dwmode* normalerweise 0 (null).</span><span class="sxs-lookup"><span data-stu-id="088ef-145">Because there is normally no need to access files, *dwMode* is typically zero.</span></span> <span data-ttu-id="088ef-146">Die-Methode speichert diese Werte nach Bedarf für den späteren Verweis.</span><span class="sxs-lookup"><span data-stu-id="088ef-146">The method stores these values as needed for later reference.</span></span>

<span data-ttu-id="088ef-147">Das folgende Code Fragment veranschaulicht, wie ein typischer shellerweiterungshandler die Methoden [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) und [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) implementiert.</span><span class="sxs-lookup"><span data-stu-id="088ef-147">The following code fragment illustrates how a typical Shell extension handler implements the [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) and [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) methods.</span></span> <span data-ttu-id="088ef-148">Es ist für die Handhabung von ANSI oder Unicode konzipiert.</span><span class="sxs-lookup"><span data-stu-id="088ef-148">It is designed to handle either ANSI or Unicode.</span></span> <span data-ttu-id="088ef-149">CLSID \_ sampleexthandler ist die GUID des Erweiterungs Handler-Objekts, und csampleshellextension ist der Name der Klasse, die zum Implementieren der Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="088ef-149">CLSID\_SampleExtHandler is the extension handler object's GUID, and CSampleShellExtension is the name of the class used to implement the interface.</span></span> <span data-ttu-id="088ef-150">Die Variablen **m \_ szFilename** und **m \_ dwmode** sind private Variablen, die zum Speichern des Namens und der Zugriffsflags der Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="088ef-150">The **m\_szFileName** and **m\_dwMode** variables are private variables that are used to store the file's name and access flags.</span></span>


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a><span data-ttu-id="088ef-151">Implementieren von ishellextinit</span><span class="sxs-lookup"><span data-stu-id="088ef-151">Implementing IShellExtInit</span></span>

<span data-ttu-id="088ef-152">Die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle verfügt über nur eine Methode, [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="088ef-152">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface has only one method, [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="088ef-153">Die-Methode verfügt über drei Parameter, die von der Shell verwendet werden können, um verschiedene Arten von Informationen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="088ef-153">The method has three parameters that the Shell can use to pass in various types of information.</span></span> <span data-ttu-id="088ef-154">Welche Werte weitergegeben werden, hängt vom Typ des Handlers ab, und einige können auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="088ef-154">The values passed in depend on the type of handler, and some can be set to **NULL**.</span></span>

-   <span data-ttu-id="088ef-155">*pidlfolder* enthält einen Ordner Zeiger auf eine Liste der Element Bezeichner (PIDL).</span><span class="sxs-lookup"><span data-stu-id="088ef-155">*pidlFolder* holds a folder's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="088ef-156">Dabei handelt es sich um eine absolute PIDL.</span><span class="sxs-lookup"><span data-stu-id="088ef-156">This is an absolute PIDL.</span></span> <span data-ttu-id="088ef-157">Bei Eigenschaften Blatt Erweiterungen ist dieser Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="088ef-157">For property sheet extensions, this value is **NULL**.</span></span> <span data-ttu-id="088ef-158">Bei Kontextmenü Erweiterungen ist dies die PIDL des Ordners, der das Element enthält, dessen Kontextmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="088ef-158">For shortcut menu extensions, it is the PIDL of the folder that contains the item whose shortcut menu is being displayed.</span></span> <span data-ttu-id="088ef-159">Bei nicht standardmäßigen Drag & Drop-Handlern ist dies die PIDL des Ziel Ordners.</span><span class="sxs-lookup"><span data-stu-id="088ef-159">For nondefault drag-and-drop handlers, it is the PIDL of the target folder.</span></span>
-   <span data-ttu-id="088ef-160">*pdataobject* enthält einen Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle eines Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="088ef-160">*pDataObject* holds a pointer to a data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="088ef-161">Das Datenobjekt enthält einen oder mehrere Dateinamen im [CF- \_ HDROP](dragdrop.md) -Format.</span><span class="sxs-lookup"><span data-stu-id="088ef-161">The data object holds one or more file names in [CF\_HDROP](dragdrop.md) format.</span></span>
-   <span data-ttu-id="088ef-162">*hregkey* enthält einen Registrierungsschlüssel für das Datei Objekt oder den Ordnertyp.</span><span class="sxs-lookup"><span data-stu-id="088ef-162">*hRegKey* holds a registry key for the file object or folder type.</span></span>

<span data-ttu-id="088ef-163">Die [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode speichert den Dateinamen, den [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger und den Registrierungsschlüssel nach Bedarf für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="088ef-163">The [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method stores the file name, [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer, and registry key as needed for later use.</span></span> <span data-ttu-id="088ef-164">Das folgende Code Fragment veranschaulicht die Implementierung von **ishellextinit:: Initialize**.</span><span class="sxs-lookup"><span data-stu-id="088ef-164">The following code fragment illustrates an implementation of **IShellExtInit::Initialize**.</span></span> <span data-ttu-id="088ef-165">Der Einfachheit halber wird in diesem Beispiel davon ausgegangen, dass das Datenobjekt nur eine einzelne Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="088ef-165">For simplicity, this example assumes that the data object contains only a single file.</span></span> <span data-ttu-id="088ef-166">Im Allgemeinen enthält das Datenobjekt möglicherweise mehrere Dateien, die jeweils extrahiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="088ef-166">In general, the data object might contain multiple files, each of which will need to be extracted.</span></span>


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a><span data-ttu-id="088ef-167">Infotip-Anpassung</span><span class="sxs-lookup"><span data-stu-id="088ef-167">Infotip Customization</span></span>

<span data-ttu-id="088ef-168">Es gibt zwei Möglichkeiten zum Anpassen von infotips.</span><span class="sxs-lookup"><span data-stu-id="088ef-168">There are two ways to customize infotips.</span></span> <span data-ttu-id="088ef-169">Eine Möglichkeit besteht darin, ein Objekt zu implementieren, das [**iqueryinfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) unterstützt, und das Objekt dann unter dem richtigen Unterschlüssel in der Registrierung zu registrieren (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="088ef-169">One way is to implement an object that supports [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) and then register the object under the proper subkey in the registry (see below).</span></span> <span data-ttu-id="088ef-170">Alternativ können Sie entweder eine festgelegte Zeichenfolge oder eine Liste bestimmter Dateieigenschaften angeben, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="088ef-170">Alternatively, you can specify either a fixed string or a list of certain file properties to be displayed.</span></span>

<span data-ttu-id="088ef-171">Um eine Zeichenfolge fester Zeichenfolge für eine Namespace Erweiterung anzuzeigen, erstellen Sie unter dem CLSID-Schlüssel der Namespace Erweiterung einen Unterschlüssel namens **infotip** .</span><span class="sxs-lookup"><span data-stu-id="088ef-171">To display a fixed string for a namespace extension, create a subkey called **InfoTip** beneath the CLSID key of your namespace extension.</span></span> <span data-ttu-id="088ef-172">Legen Sie die Daten des unter Schlüssels auf die Zeichenfolge fest, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="088ef-172">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

<span data-ttu-id="088ef-173">Um eine festgelegte Zeichenfolge für einen Dateityp anzuzeigen, erstellen Sie unter dem **ProgID** -Schlüssel des Dateityps, für den Sie Infotipps bereitstellen möchten, einen Unterschlüssel namens **infotip** .</span><span class="sxs-lookup"><span data-stu-id="088ef-173">To display a fixed string for a file type, create a subkey called **InfoTip** beneath the **ProgID** key of the file type for which you want to supply infotips.</span></span> <span data-ttu-id="088ef-174">Legen Sie die Daten des unter Schlüssels auf die Zeichenfolge fest, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="088ef-174">Set the data of that subkey to be the string you want to be displayed.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

<span data-ttu-id="088ef-175">Wenn Sie möchten, dass die Shell bestimmte Dateieigenschaften im Infotipp für einen bestimmten Dateityp anzeigt, erstellen Sie unter dem **ProgID** -Schlüssel dieses Dateityps einen Unterschlüssel namens **Infotipp** .</span><span class="sxs-lookup"><span data-stu-id="088ef-175">If you want the Shell to show certain file properties in the infotip for a specific file type, create a subkey called **InfoTip** beneath the **ProgID** key of that file type.</span></span> <span data-ttu-id="088ef-176">Legen Sie für die Daten dieses unter Schlüssels eine durch Semikolons getrennte Liste von kanonischen Eigenschaftsnamen oder {fmtid}, PID-Paare, bei denen *propName* ein kanonischer Eigenschaftsname ist *, und {fmtid}, PID* ein [**fmtid/PID-paar**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="088ef-176">Set the data of that subkey to be a semicolon-delineated list of canonical property names or {fmtid}, pid pairs where *propname* is a canonical property name and *{fmtid},pid* is a [**FMTID/PID pair**](./objects.md).</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

<span data-ttu-id="088ef-177">Die folgenden Eigenschaftsnamen können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="088ef-177">The following property names can be used.</span></span>



| <span data-ttu-id="088ef-178">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="088ef-178">Property Name</span></span>    | <span data-ttu-id="088ef-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="088ef-179">Description</span></span>                   | <span data-ttu-id="088ef-180">Abgerufen von</span><span class="sxs-lookup"><span data-stu-id="088ef-180">Retrieved From</span></span>                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="088ef-181">Autor</span><span class="sxs-lookup"><span data-stu-id="088ef-181">Author</span></span>           | <span data-ttu-id="088ef-182">Autor des Dokuments</span><span class="sxs-lookup"><span data-stu-id="088ef-182">Author of the document</span></span>        | [<span data-ttu-id="088ef-183">**pidsi- \_ Autor**</span><span class="sxs-lookup"><span data-stu-id="088ef-183">**PIDSI\_AUTHOR**</span></span>](../stg/the-summary-information-property-set.md)                             |
| <span data-ttu-id="088ef-184">Titel</span><span class="sxs-lookup"><span data-stu-id="088ef-184">Title</span></span>            | <span data-ttu-id="088ef-185">Titel des Dokuments</span><span class="sxs-lookup"><span data-stu-id="088ef-185">Title of the document</span></span>         | [<span data-ttu-id="088ef-186">**pidsi- \_ Titel**</span><span class="sxs-lookup"><span data-stu-id="088ef-186">**PIDSI\_TITLE**</span></span>](../stg/the-summary-information-property-set.md)                              |
| <span data-ttu-id="088ef-187">Subject</span><span class="sxs-lookup"><span data-stu-id="088ef-187">Subject</span></span>          | <span data-ttu-id="088ef-188">Themen Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="088ef-188">Subject summary</span></span>               | [<span data-ttu-id="088ef-189">**pidsi- \_ Betreff**</span><span class="sxs-lookup"><span data-stu-id="088ef-189">**PIDSI\_SUBJECT**</span></span>](../stg/the-summary-information-property-set.md)                            |
| <span data-ttu-id="088ef-190">Comment</span><span class="sxs-lookup"><span data-stu-id="088ef-190">Comment</span></span>          | <span data-ttu-id="088ef-191">Dokument Kommentare</span><span class="sxs-lookup"><span data-stu-id="088ef-191">Document comments</span></span>             | <span data-ttu-id="088ef-192">[**Pidsi \_ Kommentar**](../stg/the-summary-information-property-set.md) -oder Ordner-/Laufwerkeigenschaften</span><span class="sxs-lookup"><span data-stu-id="088ef-192">[**PIDSI\_COMMENT**](../stg/the-summary-information-property-set.md) or folder/drive properties</span></span> |
| <span data-ttu-id="088ef-193">PageCount</span><span class="sxs-lookup"><span data-stu-id="088ef-193">PageCount</span></span>        | <span data-ttu-id="088ef-194">Anzahl von Seiten</span><span class="sxs-lookup"><span data-stu-id="088ef-194">Number of pages</span></span>               | [<span data-ttu-id="088ef-195">**pidsi \_ Page count**</span><span class="sxs-lookup"><span data-stu-id="088ef-195">**PIDSI\_PAGECOUNT**</span></span>](../stg/the-summary-information-property-set.md)                          |
| <span data-ttu-id="088ef-196">Name</span><span class="sxs-lookup"><span data-stu-id="088ef-196">Name</span></span>             | <span data-ttu-id="088ef-197">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="088ef-197">Friendly name</span></span>                 | <span data-ttu-id="088ef-198">Standard Ordneransicht</span><span class="sxs-lookup"><span data-stu-id="088ef-198">Standard folder view</span></span>                                                                      |
| <span data-ttu-id="088ef-199">Ursprungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="088ef-199">OriginalLocation</span></span> | <span data-ttu-id="088ef-200">Speicherort der ursprünglichen Datei</span><span class="sxs-lookup"><span data-stu-id="088ef-200">Location of original file</span></span>     | <span data-ttu-id="088ef-201">Ordner "Briefkasten" und "Papierkorb"</span><span class="sxs-lookup"><span data-stu-id="088ef-201">Briefcase folder and Recycle Bin folder</span></span>                                                   |
| <span data-ttu-id="088ef-202">Datedeleted</span><span class="sxs-lookup"><span data-stu-id="088ef-202">DateDeleted</span></span>      | <span data-ttu-id="088ef-203">Die Datums Datei wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="088ef-203">Date file was deleted</span></span>         | <span data-ttu-id="088ef-204">Papierkorb Ordner</span><span class="sxs-lookup"><span data-stu-id="088ef-204">Recycle Bin folder</span></span>                                                                        |
| <span data-ttu-id="088ef-205">type</span><span class="sxs-lookup"><span data-stu-id="088ef-205">Type</span></span>             | <span data-ttu-id="088ef-206">Dateityp</span><span class="sxs-lookup"><span data-stu-id="088ef-206">Type of file</span></span>                  | <span data-ttu-id="088ef-207">Ansicht "Standard Ordner Details"</span><span class="sxs-lookup"><span data-stu-id="088ef-207">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="088ef-208">Size</span><span class="sxs-lookup"><span data-stu-id="088ef-208">Size</span></span>             | <span data-ttu-id="088ef-209">Größe der Datei</span><span class="sxs-lookup"><span data-stu-id="088ef-209">Size of file</span></span>                  | <span data-ttu-id="088ef-210">Ansicht "Standard Ordner Details"</span><span class="sxs-lookup"><span data-stu-id="088ef-210">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="088ef-211">Synccopyin</span><span class="sxs-lookup"><span data-stu-id="088ef-211">SyncCopyIn</span></span>       | <span data-ttu-id="088ef-212">Identisch mit "Ursprungs Zuordnung"</span><span class="sxs-lookup"><span data-stu-id="088ef-212">Same as OriginalLocation</span></span>      | <span data-ttu-id="088ef-213">Identisch mit "Ursprungs Zuordnung"</span><span class="sxs-lookup"><span data-stu-id="088ef-213">Same as OriginalLocation</span></span>                                                                  |
| <span data-ttu-id="088ef-214">Geändert</span><span class="sxs-lookup"><span data-stu-id="088ef-214">Modified</span></span>         | <span data-ttu-id="088ef-215">Datum der letzten Änderung</span><span class="sxs-lookup"><span data-stu-id="088ef-215">Date last modified</span></span>            | <span data-ttu-id="088ef-216">Ansicht "Standard Ordner Details"</span><span class="sxs-lookup"><span data-stu-id="088ef-216">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="088ef-217">Erstellt</span><span class="sxs-lookup"><span data-stu-id="088ef-217">Created</span></span>          | <span data-ttu-id="088ef-218">Erstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="088ef-218">Date created</span></span>                  | <span data-ttu-id="088ef-219">Ansicht "Standard Ordner Details"</span><span class="sxs-lookup"><span data-stu-id="088ef-219">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="088ef-220">Auf</span><span class="sxs-lookup"><span data-stu-id="088ef-220">Accessed</span></span>         | <span data-ttu-id="088ef-221">Datum des letzten Zugriffs</span><span class="sxs-lookup"><span data-stu-id="088ef-221">Date last accessed</span></span>            | <span data-ttu-id="088ef-222">Ansicht "Standard Ordner Details"</span><span class="sxs-lookup"><span data-stu-id="088ef-222">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="088ef-223">InFolder</span><span class="sxs-lookup"><span data-stu-id="088ef-223">InFolder</span></span>         | <span data-ttu-id="088ef-224">Verzeichnis, das die Datei enthält</span><span class="sxs-lookup"><span data-stu-id="088ef-224">Directory containing the file</span></span> | <span data-ttu-id="088ef-225">Dokument Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="088ef-225">Document search results</span></span>                                                                   |
| <span data-ttu-id="088ef-226">Rang</span><span class="sxs-lookup"><span data-stu-id="088ef-226">Rank</span></span>             | <span data-ttu-id="088ef-227">Qualität der Such Übereinstimmung</span><span class="sxs-lookup"><span data-stu-id="088ef-227">Quality of search match</span></span>       | <span data-ttu-id="088ef-228">Dokument Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="088ef-228">Document search results</span></span>                                                                   |
| <span data-ttu-id="088ef-229">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="088ef-229">FreeSpace</span></span>        | <span data-ttu-id="088ef-230">Verfügbarer Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="088ef-230">Available storage space</span></span>       | <span data-ttu-id="088ef-231">Laufwerke</span><span class="sxs-lookup"><span data-stu-id="088ef-231">Disk drives</span></span>                                                                               |
| <span data-ttu-id="088ef-232">Anzahl von besuchen</span><span class="sxs-lookup"><span data-stu-id="088ef-232">NumberOfVisits</span></span>   | <span data-ttu-id="088ef-233">Anzahl von Aufrufen</span><span class="sxs-lookup"><span data-stu-id="088ef-233">Number of visits</span></span>              | <span data-ttu-id="088ef-234">Ordner "Favoriten"</span><span class="sxs-lookup"><span data-stu-id="088ef-234">Favorites folder</span></span>                                                                          |
| <span data-ttu-id="088ef-235">Attributes</span><span class="sxs-lookup"><span data-stu-id="088ef-235">Attributes</span></span>       | <span data-ttu-id="088ef-236">Dateiattribute</span><span class="sxs-lookup"><span data-stu-id="088ef-236">File Attributes</span></span>               | <span data-ttu-id="088ef-237">Ansicht "Standard Ordner Details"</span><span class="sxs-lookup"><span data-stu-id="088ef-237">Standard folder details view</span></span>                                                              |
| <span data-ttu-id="088ef-238">Company</span><span class="sxs-lookup"><span data-stu-id="088ef-238">Company</span></span>          | <span data-ttu-id="088ef-239">Unternehmensname</span><span class="sxs-lookup"><span data-stu-id="088ef-239">Company name</span></span>                  | [<span data-ttu-id="088ef-240">**piddsi- \_ Unternehmen**</span><span class="sxs-lookup"><span data-stu-id="088ef-240">**PIDDSI\_COMPANY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| <span data-ttu-id="088ef-241">Kategorie</span><span class="sxs-lookup"><span data-stu-id="088ef-241">Category</span></span>         | <span data-ttu-id="088ef-242">Dokument Kategorie</span><span class="sxs-lookup"><span data-stu-id="088ef-242">Document category</span></span>             | [<span data-ttu-id="088ef-243">**piddsi- \_ Kategorie**</span><span class="sxs-lookup"><span data-stu-id="088ef-243">**PIDDSI\_CATEGORY**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| <span data-ttu-id="088ef-244">Copyright</span><span class="sxs-lookup"><span data-stu-id="088ef-244">Copyright</span></span>        | <span data-ttu-id="088ef-245">Medien Copyright</span><span class="sxs-lookup"><span data-stu-id="088ef-245">Media copyright</span></span>               | [<span data-ttu-id="088ef-246">**pidmsi \_ Copyright**</span><span class="sxs-lookup"><span data-stu-id="088ef-246">**PIDMSI\_COPYRIGHT**</span></span>](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| <span data-ttu-id="088ef-247">Htmlinfotipfile</span><span class="sxs-lookup"><span data-stu-id="088ef-247">HTMLInfoTipFile</span></span>  | <span data-ttu-id="088ef-248">HTML-infotip-Datei</span><span class="sxs-lookup"><span data-stu-id="088ef-248">HTML InfoTip file</span></span>             | <span data-ttu-id="088ef-249">Datei für Ordner Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="088ef-249">Desktop.ini file for folder</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="088ef-250">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="088ef-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="088ef-251">Registrieren von Shellerweiterungs Handlern</span><span class="sxs-lookup"><span data-stu-id="088ef-251">Registering Shell Extension Handlers</span></span>](reg-shell-exts.md)
</dt> </dl>

 

 
