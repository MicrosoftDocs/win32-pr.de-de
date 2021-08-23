---
description: Die IWiaImageFilter-Schnittstelle ist eine Erweiterungsschnittstelle, die von Bildverarbeitungsfilterentwicklern implementiert und von Windows Image Acquisition (WIA) 2.0 aufgerufen wird.
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: IWiaImageFilter-Schnittstelle (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: d7c85a25d7478e0ad51a1d427e74b69a743bc4203ed57b8929a3e4ec856d94b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813980"
---
# <a name="iwiaimagefilter-interface"></a>IWiaImageFilter-Schnittstelle

Die **IWiaImageFilter-Schnittstelle** ist eine Erweiterungsschnittstelle, die von Entwicklern von Bildverarbeitungsfiltern implementiert und von Windows Image Acquisition (WIA) 2.0 aufgerufen wird.

## <a name="members"></a>Member

Die **IWiaImageFilter-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaImageFilter** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaImageFilter-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ApplyProperties**](-wia-iwiaimagefilter-applyproperties.md)       | Aktiviert den Filter für die Bildverarbeitung, um Eigenschaften zurück in den Treiber (und das Gerät) zu schreiben.<br/>     |
| [**FilterPreviewImage**](-wia-iwiaimagefilter-filterpreviewimage.md) | Filtert das Vorschaubild.<br/>                                                                   |
| [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)     | Initialisiert den Filter. Wird von WIA 2.0 vor jedem Imagedownload aufgerufen. <br/>                       |
| [**SetNewCallback**](-wia-iwiaimagefilter-setnewcallback.md)         | Legt einen neuen Anwendungsrückruf für den Bildverarbeitungsfilter fest, der für die Weiterleitung von Aufrufen verwendet werden soll.<br/> |



 

## <a name="remarks"></a>Hinweise

Entwickler von Bildverarbeitungsfiltern sollten diese Schnittstelle und die [**IWiaTransferCallback-Schnittstelle**](-wia-iwiatransfercallback.md) implementieren.

WIA 2.0 ruft Filtermethoden auf. Sie werden nie direkt aus einer Anwendung aufgerufen.

Microsoft stellt die WIA 2.0 Preview-Komponente zur Verfügung, die das ursprüngliche, ungefilterte Vorschaubild zwischenspeichert, das vom Scanner bezogen wird. Eine Anwendung verwendet [CoCreateInstance,](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um eine Instanz der WIA 2.0-Vorschaukomponente (CLSID WiaPreview) zu erstellen, \_ die den Filter mit [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md)lädt. Der Filter wird automatisch aufgerufen, wenn die Anwendung [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md)aufruft.

Der Bildverarbeitungsfilter wird immer ausgeführt, wenn ein Bild gescannt wird. Eine Anwendung kann kein Bild vom Scanner abrufen, ohne dass zuerst der Bildverarbeitungsfilter angewendet wird.

Ein Filter muss mindestens Helligkeit und Kontrast implementieren. Die allgemeine Benutzeroberfläche, die dem Benutzer Helligkeits- und Kontraststeuerelemente bereitstellt, kann dem Benutzer genaue Vorschauen anzeigen.

Ein Bildverarbeitungsfilter sollte niemals den *lMessage-Member* der [**WiaTransferParams-Struktur**](-wia-wiatransferparams.md) ändern.

Um die erforderlichen Eigenschaften zu lesen, sollte der Bildverarbeitungsfilter [**IWiaPropertyStorage::GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) auf der [**IWiaPropertyStorage-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) aufrufen, die er aus dem Element abruft, indem [er IWiaImageFilter::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))aufruft. Der Filter kann dann eine [IPropertyStorage-Instanz](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) in diesem Stream instanziieren, um die Elementeigenschaften zu lesen. Der Bildverarbeitungsfilter sollte [IWiaPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) nicht direkt aufrufen, da diese Methode den `drvReadItemProperties` aufruft, aber der WIA 2.0-Dienst den Treiber bereits im Aufruf gesperrt hat, `drvAcquireItemData` sodass bei diesem Aufruf ein Timeout auftritt und ein Fehler auftritt.

Die Eigenschaften, an denen der Filter interessiert ist, können z. B. die Helligkeits- und Kontrasteinstellungen sein. Der Filter muss in der Regel auch das Bildformat sowie die Vorschaueigenschaft [**WIA \_ DPS \_ PREVIEW**](-wia-wiaitempropscannerdevice.md)aus *pWiaItem2* lesen. Diese Eigenschaften werden alle im Filterprozess verwendet.

Die WIA 2.0-Komponenten schreiben immer ungefilterte Daten in den Bildverarbeitungsfilter. Der vom Datenstrom des Filters implementierte Bildverarbeitungsalgorithmus kann die Daten mehr als einmal filtern und muss sich nicht darum kümmern, die gleichen Ergebnisse wie das einmalige Filtern der Daten zu erzeugen.

Der Filter muss auf die [**WIA \_ DPS \_ PREVIEW-Eigenschaft**](-wia-wiaitempropscannerdevice.md) achten, insbesondere wenn einige filterbezogene Aufgaben in der Hardware verarbeitet werden. Beispielsweise kann ein bestimmter Treiber die Helligkeit der Lampe in der Scannerhardware ändern, je nachdem, wie die Anwendung die Helligkeit in ein WIA 2.0-Element festgelegt hat. Während der letzten Überprüfung (wenn die Anwendung [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md)aufruft) ändert der Treiber in der Regel die physische Lampe des Scanners. In diesem Fall muss der Bildverarbeitungsfilter möglicherweise überhaupt keine Helligkeitsverarbeitung durchführen. Während einer Vorschauüberprüfung sollte der Treiber jedoch die Helligkeit der Lampe nicht ändern. Stattdessen sollte dies ausschließlich im Bildverarbeitungsfilter berücksichtigt werden. Es ist wichtig, dass die WIA 2.0-Vorschaukomponente und der Bildverarbeitungsfilter genaue Bilder basierend auf den eigenschaften zurückgeben, die im Element festgelegt sind.

Ein Bildverarbeitungsfilter muss alle Bildformate unterstützen, die der Treiber unterstützt.

Dem Bildverarbeitungsfilter wird immer ein Bild angezeigt, das dem Auswahlbereich entspricht, der in dem Element festgelegt ist, für das wir das Bild abrufen. Beachten Sie jedoch, dass das Bild möglicherweise vom Treiber gedreht wurde, falls es die [**WIA \_ IPS \_ ROTATION-Eigenschaft**](-wia-wiaitempropscanneritem.md) unterstützt.

Der Bildverarbeitungsfilter wird über [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md)erstellt, in der Regel nicht von der Anwendung, sondern von WIA 2.0-Komponenten, wenn eine Anwendung [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) oder [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md)aufruft.

Die **IWiaImageFilter-Schnittstelle** erbt wie alle com-Schnittstellen (Component Object Model) die [IUnknown-Schnittstellenmethoden.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| IUnknown-Methoden                                        | Beschreibung                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
