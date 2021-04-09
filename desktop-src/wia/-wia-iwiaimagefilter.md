---
description: Die iwiaimagefilter-Schnittstelle ist eine durch Bild Verarbeitungs Filter-Entwickler implementierte Erweiterungsschnittstelle, die von der Windows-Abbild Erfassung (WIA) 2,0 aufgerufen wird.
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: Iwiaimagefilter-Schnittstelle (WIA. h)
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
ms.openlocfilehash: 8d859b79d15db627bb09cb60f758791a8b5860f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865240"
---
# <a name="iwiaimagefilter-interface"></a>Iwiaimagefilter-Schnittstelle

Die **iwiaimagefilter** -Schnittstelle ist eine durch Bild Verarbeitungs Filter-Entwickler implementierte Erweiterungsschnittstelle, die von der Windows-Abbild Erfassung (WIA) 2,0 aufgerufen wird.

## <a name="members"></a>Member

Die **iwiaimagefilter** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwiaimagefilter** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwiaimagefilter** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Applyproperties**](-wia-iwiaimagefilter-applyproperties.md)       | Ermöglicht dem Bild Verarbeitungs Filter das Zurückschreiben von Eigenschaften an den Treiber (und das Gerät).<br/>     |
| [**FilterPreviewImage**](-wia-iwiaimagefilter-filterpreviewimage.md) | Filtert das Vorschaubild.<br/>                                                                   |
| [**Initializefilter**](-wia-iwiaimagefilter-initializefilter.md)     | Initialisiert den Filter. Wird von WIA 2,0 vor jedem Bilddownload aufgerufen. <br/>                       |
| [**Setnewcallback**](-wia-iwiaimagefilter-setnewcallback.md)         | Legt einen neuen Anwendungs Rückruf für den Bild Verarbeitungs Filter fest, der für Weiterleitungs Aufrufe verwendet werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Bild Verarbeitungs Filter-Entwickler sollten diese Schnittstelle und die [**iwiatransfercallback**](-wia-iwiatransfercallback.md) -Schnittstelle implementieren.

WIA 2,0 ruft Filter Methoden auf. Sie werden niemals direkt von einer Anwendung aufgerufen.

Microsoft stellt die WIA 2,0 Preview-Komponente bereit, die das ursprüngliche, ungefilterte Vorschaubild zwischenspeichert, das vom Scanner abgerufen wird. Eine Anwendung verwendet [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , um eine Instanz der WIA 2,0-Vorschau Komponente (CLSID \_ wiapreview) zu erstellen, die den Filter mithilfe von [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md)lädt. Der Filter wird automatisch aufgerufen, wenn die Anwendung [**iwiatransfer::D ownload**](-wia-iwiatransfer-download.md)aufruft.

Der Bild Verarbeitungs Filter wird immer ausgeführt, wenn ein Bild gescannt wird. Eine Anwendung kann kein Image vom Scanner abrufen, ohne dass der Bild Verarbeitungs Filter zuerst angewendet wird.

Ein Filter muss die Helligkeit und den Kontrast minimal implementieren. Die gemeinsame Benutzeroberfläche, die dem Benutzer Helligkeit und Kontrast Steuerelemente bereitstellt, kann dem Benutzer genaue Vorschau anzeigen.

Ein Bild Verarbeitungs Filter sollte nie den *lMessage* -Member der [**wiatransferparameams**](-wia-wiatransferparams.md) -Struktur ändern.

Um die erforderlichen Eigenschaften zu lesen, sollte der Bild Verarbeitungs Filter [**iwiapropertystorage:: getpropertystream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) auf der [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle aufrufen, die er vom Element erhält, indem er [iwiaimagefilter:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))aufruft. Der Filter kann dann eine [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) -Instanz in diesem Stream instanziieren, um die Element Eigenschaften zu lesen. Der Bild Verarbeitungs Filter sollte [iwiapropertystorage:: Read Multiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) nicht direkt aufrufen, da diese Methode den Treiber aufruft `drvReadItemProperties` , aber der WIA 2,0-Dienst den Treiber bereits im Aufruf gesperrt hat, `drvAcquireItemData` sodass dieser Aufruf einen Timeout und einen Fehler verursacht.

Die Eigenschaften, an denen der Filter interessiert ist, könnten z. b. die Einstellungen für Helligkeit und Kontrast sein. Der Filter muss in der Regel auch das Bildformat und die Vorschau Eigenschaft ( [**WIA \_ DPS \_ Preview**](-wia-wiaitempropscannerdevice.md)) von *pWiaItem2* lesen. Diese Eigenschaften werden alle im Filter Vorgang verwendet.

Die WIA 2,0-Komponenten schreiben immer ungefilterte Daten in den Bild Verarbeitungs Filter. Der vom Stream des Filters implementierte Bild Verarbeitungs Algorithmus kann die Daten mehrmals Filtern und muss sich nicht darum kümmern, dieselben Ergebnisse wie das Filtern der Daten zu erzeugen.

Der Filter muss auf die [**\_ \_ Vorschau Eigenschaft der WIA-DPS**](-wia-wiaitempropscannerdevice.md) achten, insbesondere, wenn einige Filter bezogene Aufgaben in der Hardware behandelt werden. Beispielsweise kann ein bestimmter Treiber die Helligkeit der Lamp in der Überprüfungs Hardware ändern, je nachdem, wie die Anwendung die Helligkeit in einem WIA-2,0-Element festgelegt hat. Während der letzten Überprüfung (wenn die Anwendung [**iwiatransfer::D ownload**](-wia-iwiatransfer-download.md)aufruft), würde der Treiber normalerweise die physische Lamp des Scanners ändern. In diesem Fall muss der Bild Verarbeitungs Filter möglicherweise überhaupt keine Helligkeits Verarbeitung durchführen. Während einer Vorschau Prüfung sollte der Treiber jedoch die Helligkeit der Lamp nicht ändern – stattdessen sollte dieser nur im Bild Verarbeitungs Filter behandelt werden. Es ist wichtig, dass die WIA 2,0-Vorschau Komponente und der Bild Verarbeitungs Filter basierend auf den Eigenschaften, die in das Element festgelegt werden, genaue Bilder zurückgeben.

Ein Bild Verarbeitungs Filter muss alle Bildformate unterstützen, die vom Treiber unterstützt werden.

Der Bild Verarbeitungs Filter erhält immer ein Bild, das dem Auswahlbereich entspricht, der auf das Element festgelegt ist, für das das Bild abgerufen wird. Beachten Sie jedoch, dass das Bild möglicherweise durch den Treiber gedreht wurde, wenn es die WIA-Eigenschaft für die [**\_ \_ Rotation von IPS**](-wia-wiaitempropscanneritem.md) unterstützt.

Der Bild Verarbeitungs Filter wird über [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md)erstellt, normalerweise nicht durch die Anwendung, sondern durch WIA 2,0-Komponenten, wenn eine Anwendung [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) oder [**iwiatransfer::D ownload**](-wia-iwiatransfer-download.md)aufruft.

Die **iwiaimagefilter** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.



| IUnknown-Methoden                                        | BESCHREIBUNG                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
