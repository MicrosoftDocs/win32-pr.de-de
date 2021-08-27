---
title: Onlinedruck-Assistent
description: Der Windows Vista Online Printing Wizard unterstützt Benutzer beim Bestellen von Fotos von beteiligten Onlinedruckhändlern.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Onlinedruck-Assistent
- Symbole,Onlinedruck-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc402f1fe5853c7a255ea45940d62efcd092c424be6905287315c5cfe5fc7504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975918"
---
# <a name="online-printing-wizard"></a>Onlinedruck-Assistent

Der Windows Vista Online Printing Wizard unterstützt Benutzer beim Bestellen von Fotos von beteiligten Onlinedruckhändlern. Dieser Assistent ist so konzipiert, dass er programmgesteuert von jeder Anwendung aufgerufen werden kann, die Benutzern die Möglichkeit bieten möchte, Fotos zu bestellen. Der Fotodruck-Assistent ist auf Windows Vista verfügbar. PIX für Windows

-   [Vom Onlinedruck-Assistenten bereitgestellte Funktionen](#features-provided-by-the-online-print-wizard)
-   [Unterstützte Fotodateiformate](#supported-photo-file-formats)
-   [Programmgesteuertes Starten des Onlinedruck-Assistenten](#programmatically-launching-the-online-print-wizard)
-   [Zugreifen auf das Symbol des Onlinedruck-Assistenten](#accessing-the-online-print-wizard-icon)
-   [MRU-Eigenschaften des Onlinedruck-Assistenten](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Vom Onlinedruck-Assistenten bereitgestellte Funktionen

Mit Windows Vista Online Printing Wizard können Benutzer Drucke von einer Auswahl teilnehmender Onlinedruckhändler bestellen. Wenn der Assistent aufgerufen wird, führt er die folgenden Schritte aus:

1.  Akzeptiert eine Datei oder Liste von Dateien, für die Drucke geordnet werden sollen.
2.  Ruft automatisch die aktuelle Liste der beteiligten Onlinedruckhändler ab und ermöglicht es dem Benutzer, den Einzelhändler auszuwählen, von dem die Fotodrucke kaufen werden.
3.  Führt den Benutzer durch den Prozess oder die Reihenfolge der Drucke.

Jede Anwendung kann von den Features profitieren, die vom Windows Vista Online Printing Wizard angeboten werden. Eine Anwendung muss nur die Dateien übergeben, für die Drucke bestellt werden, und der Assistent führt den Benutzer durch den Bestellvorgang.

Die folgende Abbildung zeigt den Windows Vista Online Printing Wizard mit einer Beispielliste der beteiligten Onlinedruckhändler.

![Der Windows Vista-Onlinedruck-Assistent](images/opw.png)

## <a name="supported-photo-file-formats"></a>Unterstützte Fotodateiformate

Der Windows Vista Online Printing Wizard unterstützt jedes Bilddateiformat, für das ein WIC-Codec (Windows Imaging Component) installiert ist. WIC bietet mehrere Standardcodecs, darunter:

-   Bitmap (BMP)
-   GIF (Graphics Interchange Format)
-   Symbolformat (ICO)
-   JPEG (Joint Photographic Experts Group)
-   PNG (Portable Network Graphics)
-   TIFF (Tagged Image File Format)
-   Windows Medienfotoformat

Weitere Informationen zu WIC- und WIC-Codecs finden Sie unter [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

Dateiformate, die von Onlinedruckhändlern unterstützt werden, variieren je nach Einzelhändler. Es ist möglich, dass ein bestimmter Einzelhändler möglicherweise nicht alle Dateiformate unterstützt, die vom Windows Vista Online Printing Wizard unterstützt werden. Wenn der Benutzer versucht, Drucke in einem Format zu bestellen, das vom ausgewählten Einzelhändler nicht unterstützt wird, benachrichtigt der Windows Vista Online Printing Wizard den Benutzer darüber, dass der ausgewählte Einzelhändler das übermittelte Dateiformat nicht unterstützt.

## <a name="programmatically-launching-the-online-print-wizard"></a>Programmgesteuertes Starten des Onlinedruck-Assistenten

Rufen Sie zum Aufrufen Windows Vista Online Printing Wizard die [IDropTarget-Schnittstelle](/windows/win32/api/oleidl/nn-oleidl-idroptarget) mit dem folgenden Klassenbezeichner (CLSID) auf:


```
CLSID_PublishDropTarget
```



Diese CLSID wird in Shobjidl.h und Shobjidl.idl definiert. Die Dateien, die vom Assistenten für Windows Vista Online Printing verarbeitet werden sollen, werden in einem [IDataObject-Objekt](/windows/win32/api/objidl/nn-objidl-idataobject) angegeben.

Im folgenden Codebeispiel wird veranschaulicht, wie der Windows Vista Online Printing Wizard aufgerufen wird.


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a>Zugreifen auf das Symbol des Onlinedruck-Assistenten

Der Windows Vista Online Printing Wizard exportiert ein Symbol, auf das von Anwendungen zugegriffen und angezeigt werden kann, die es aufrufen. Die folgende Abbildung zeigt das Symbol Windows Vista Online Printing Wizard( Vista-Onlinedruck-Assistent).

![Das Symbol des Onlinedruck-Assistenten für Windows Vista](images/opw-icon.png)

Im folgenden Codebeispiel wird veranschaulicht, wie sie den Index für das Symbol Windows Vista Online Printing Wizard abrufen, indem Sie die **OPWIcon-Eigenschaft** lesen.


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a>MRU-Eigenschaften des Onlinedruck-Assistenten

Der Windows Vista Online Printing Wizard definiert drei Eigenschaften, die sich auf den zuletzt verwendeten Onlinedruckhändler (MRU) bezieht.



| Eigenschaftsname | Eigenschaftswert/Funktion                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MRUIcon**   | Der Index des Symbols für den zuletzt verwendeten Onlinedruckhändler kann aus dieser Eigenschaft gelesen werden.                                                                                                                                                                 |
| **MRUName**   | Der Name des zuletzt verwendeten Onlinedruckhändlers kann aus dieser Eigenschaft gelesen werden.                                                                                                                                                                               |
| **UseMRU**    | Ein **VARIANT** **VT \_ BOOL-Wert,** der angibt, ob der Assistent die Auswahlseite des Onlinedruckhändlers überspringen und stattdessen nur den zuletzt verwendeten Onlinedruckhändler verwenden soll. Legen Sie diese Eigenschaft auf **VARIANT \_ TRUE fest,** um die Auswahlseite des Einzelhändlers zu überspringen. |



 

Im folgenden Codebeispiel wird veranschaulicht, wie die UseMRU-Eigenschaft so festgelegt wird, dass der Windows Vista Online Printing Wizard die Auswahlseite des Onlinedruckhändlers umgeht und automatisch den zuletzt verwendeten Einzelhändler auswählt.


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



Im folgenden Codebeispiel wird veranschaulicht, wie die Eigenschaften MRUName und MRUIcon gelesen werden.


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 