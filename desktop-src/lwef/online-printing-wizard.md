---
title: Online Druck-Assistent
description: Der Windows Vista-Online Druck-Assistent unterstützt Benutzer beim Sortieren von Fotos aus teilnehmenden Online Druck-Einzelhandels Händlern.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Online Druck-Assistent
- Symbole, Online Druck-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315093"
---
# <a name="online-printing-wizard"></a>Online Druck-Assistent

Der Windows Vista-Online Druck-Assistent unterstützt Benutzer beim Sortieren von Fotos aus teilnehmenden Online Druck-Einzelhandels Händlern. Dieser Assistent ist so konzipiert, dass er Programm gesteuert von jeder Anwendung aufgerufen werden kann, die Benutzern die Möglichkeit bietet, Fotos von Fotos zu bestellen. Der Fotodruck-Assistent ist unter Windows Vista verfügbar. Pix für Windows

-   [Vom Online Druck-Assistenten bereitgestellte Funktionen](#features-provided-by-the-online-print-wizard)
-   [Unterstützte Foto Dateiformate](#supported-photo-file-formats)
-   [Programm gesteuertes Starten des Online Druck-Assistenten](#programmatically-launching-the-online-print-wizard)
-   [Zugreifen auf das Symbol für den Online Druck-Assistenten](#accessing-the-online-print-wizard-icon)
-   [MRU-Eigenschaften des Online Druck-Assistenten](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Vom Online Druck-Assistenten bereitgestellte Funktionen

Der Windows Vista-Online Druck-Assistent ermöglicht Benutzern das Sortieren von Druck Vorgängen aus einer Auswahl von teilnehmenden Online Druck-Einzelhandels Händlern. Wenn der Assistent aufgerufen wird, wird Folgendes ausgeführt:

1.  Akzeptiert eine Datei oder eine Liste von Dateien, für die gedruckt werden sollen.
2.  Ruft automatisch die aktuelle Liste der teilnehmenden Online Druck Händler ab und ermöglicht dem Benutzer, den Einzelhändler auszuwählen, von dem die Foto Abdrücke gekauft werden.
3.  Führt den Benutzer durch den Prozess oder die Reihenfolge der Ausdrucke.

Jede Anwendung kann von den Funktionen profitieren, die vom Windows Vista-Online Druck-Assistenten angeboten werden. Eine Anwendung muss nur die Datei oder Dateien übergeben, für die gedruckt werden, und der Assistent führt den Benutzer durch den Bestellvorgang.

Die folgende Abbildung zeigt den Windows Vista-Online Druck-Assistenten, der eine Beispielliste der teilnehmenden Online Druck-Einzelhändler anzeigt.

![der Windows Vista-Online Druck-Assistent](images/opw.png)

## <a name="supported-photo-file-formats"></a>Unterstützte Foto Dateiformate

Der Windows Vista-Online Druck-Assistent unterstützt alle Bild Dateiformate, für die ein WIC-Codec (Windows Imaging Component) installiert ist. WIC bietet mehrere Standard-Codecs, einschließlich:

-   Bitmap (BMP)
-   GIF (Graphics Interchange Format)
-   Symbol Format (ICO)
-   JPEG (Joint Photographic Experts Group)
-   PNG (Portable Network Graphics)
-   TIFF (Tagged Image File Format)
-   Windows Media-Fotoformat

Weitere Informationen zu WIC-und WIC-Codecs finden Sie unter [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

Dateiformate, die von Online Druck-Einzelhändlern unterstützt werden, variieren je nach Einzelhändler möglicherweise unterstützt ein bestimmter Einzelhändler nicht alle Dateiformate, die vom Windows Vista-Online Druck-Assistenten unterstützt werden. Wenn der Benutzer versucht, Druck in einem Format zu sortieren, das vom ausgewählten Einzelhändler nicht unterstützt wird, benachrichtigt der Windows Vista-Online Druck-Assistent den Benutzer, dass der ausgewählte Einzelhändler das Format der übermittelten Dateien nicht unterstützt.

## <a name="programmatically-launching-the-online-print-wizard"></a>Programm gesteuertes Starten des Online Druck-Assistenten

Um den Windows Vista-Online Druck-Assistenten aufzurufen, rufen Sie die [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle mit der folgenden Klassen Kennung (CLSID) auf:


```
CLSID_PublishDropTarget
```



Diese CLSID ist in "shobjidl. h" und "shobjidl. idl" definiert. Die Dateien, die vom Windows Vista-Online Druck-Assistenten verarbeitet werden sollen, werden in einem [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) -Objekt angegeben.

Im folgenden Codebeispiel wird veranschaulicht, wie der Windows Vista-Online Druck-Assistent aufgerufen wird.


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



## <a name="accessing-the-online-print-wizard-icon"></a>Zugreifen auf das Symbol für den Online Druck-Assistenten

Der Windows Vista-Online Druck-Assistent exportiert ein Symbol, auf das zugegriffen werden kann und das von Anwendungen angezeigt wird, die es aufrufen. In der folgenden Abbildung ist das Symbol für den Windows Vista-Online Druck-Assistenten dargestellt.

![Symbol für den Windows Vista-Online Druck-Assistenten](images/opw-icon.png)

Im folgenden Codebeispiel wird veranschaulicht, wie der Index für das Windows Vista-Online Druck-Assistenten Symbol abgerufen wird, indem die **opwicon** -Eigenschaft gelesen wird.


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



## <a name="online-print-wizard-mru-properties"></a>MRU-Eigenschaften des Online Druck-Assistenten

Der Windows Vista-Online Druck-Assistent definiert drei Eigenschaften, die mit dem zuletzt verwendeten (MRU) Online Druck-Einzelhändler verknüpft sind.



| Eigenschaftsname | Eigenschafts Wert/-Funktion                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mruicon**   | Der Index des Symbols für den zuletzt verwendeten Online Druck-Einzelhändler kann aus dieser Eigenschaft gelesen werden.                                                                                                                                                                 |
| **Mruname**   | Der Name des zuletzt verwendeten Online Druck-Einzelhandels Händlers kann aus dieser Eigenschaft gelesen werden.                                                                                                                                                                               |
| **Usemru**    | Ein **variabler** **VT- \_ boolescher** Wert, der angibt, ob der Assistent die Auswahl Seite für den Online Druck-Einzelhandel überspringen soll, und stattdessen nur den zuletzt verwendeten Online Druck Händler verwenden. Legen Sie diese Eigenschaft auf **Variant \_ true** fest, um die Auswahl Seite für den Händler zu überspringen |



 

Im folgenden Codebeispiel wird veranschaulicht, wie die usemru-Eigenschaft festgelegt wird, sodass der Windows Vista-Online Druck-Assistent die Auswahl Seite für den Online Druck-Einzelhandel umgeht und automatisch den zuletzt verwendeten Einzelhändler auswählt.


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



Im folgenden Codebeispiel wird veranschaulicht, wie die Eigenschaften mruname und mruicon gelesen werden.


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



 

 