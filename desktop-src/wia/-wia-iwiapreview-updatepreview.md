---
description: 'Ruft das ungefilterte Bild ab, das von der iwiapreview:: getnewpreview-Methode zwischengespeichert wird.'
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'Iwiapreview:: updatepreview-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129417"
---
# <a name="iwiapreviewupdatepreview-method"></a>Iwiapreview:: updatepreview-Methode

Ruft das ungefilterte Bild ab, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*loptions* \[ in\]
</dt> <dd>

Type: **Long**

Gibt an, ob die Anwendung die WIA 2,0-Vorschau Komponente benötigt, um einen Teilbereich des zwischengespeicherten Bilds oder das gesamte zwischengespeicherte Bild an den Bild Verarbeitungs Filter zu übergeben.

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**Wiapreviewreturnoriginalimage**


</dt> <dd>

Übergeben Sie das gesamte zwischengespeicherte Bild an den Bild Verarbeitungs Filter.

</dd> </dl> </dd> <dt>

*pchildwiaitem* \[ in\]
</dt> <dd>

Typ: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Gibt einen Zeiger auf das [_ *IWiaItem2* *](-wia-iwiaitem2.md) -Element an, das ein untergeordnetes Element des **IWiaItem2** -Elements ist, das durch den *pWiaItem2* -Parameter der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode angegeben wird. Wenn die Anwendung eine Vorschau des gesamten Flatbed erfordert, gibt einen Zeiger auf den *pWiaItem2* -Parameter der **iwiapreview:: getnewpreview** -Methode an. Wenn *pchildwiaitem* ein untergeordnetes Element des *pWiaItem2* -Parameters von **iwiapreview:: getnewpreview** ist, wird dieses untergeordnete Element normalerweise vom Segmentierungs Filter erstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode übergibt das zwischengespeicherte, ungefilterte Bild über den Bild Verarbeitungs Filter, der dann die gefilterten Daten in den von der Anwendung bereitgestellten Stream schreibt. Die WIA 2,0-Vorschau Komponente ruft diesen Stream durch Aufrufen der [**getnextstream**](-wia-iwiatransfercallback-getnextstream.md) -Methode des Bild Verarbeitungs Filters ab, die dann die **getnextstream** -Implementierung des Anwendungs Rückrufs aufruft. Vor dem Aufrufen von **iwiapreview:: updatepreview** muss eine Anwendung zuerst [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) aufrufen, um das Image vom Scanner abzurufen. Andernfalls gibt die Methode einen Fehler zurück.

Die WIA 2,0-Vorschau Komponente speichert das ungefilterte Bild, das vom Treiber heruntergeladen wurde. Es ist möglich, dass das an **iwiapreview:: updatepreview** übergebenen WIA 2,0-Element nur einen kleinen Bereich des vom Treiber heruntergeladenen Bilds darstellt. Wenn dies der Fall ist, schneidet die WIA 2,0-Vorschau Komponente diese Region tatsächlich aus dem zwischengespeicherten Image aus, bevor Sie Sie an den Bild Verarbeitungs Filter übergibt, der wiederum die gefilterten Bilddaten an die Anwendung zurück übergibt.

Damit eine Anwendung das gesamte zwischengespeicherte Bild an den Bild Verarbeitungs Filter übergibt (der wiederum an die Anwendung übergeben wird), muss die *loptions* beim Aufrufen von **iwiapreview:: updatepreview** auf **wiapreviewreturnoriginalimage** festgelegt werden. Wenn *loptions* auf **wiapreviewreturnoriginalimage** festgelegt wird, muss die Anwendung sicherstellen, dass die Block Einstellungen ([**WIA \_ IPS \_ xblock**](-wia-wiaitempropscanneritem.md) und **WIA \_ IPS \_ yblock**) des an **iwiapreview:: updatepreview** übergebenen Elements mit dem vollständig zwischengespeicherten Image übereinstimmen. Der Bild Verarbeitungs Filter muss in diesem Fall nichts unterscheiden. das Image wird einfach basierend auf den Eigenschaften von *pchildwiaitem* gefiltert (in diesem Fall ist *pchildwiaitem* dasselbe Element, das an [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)übergeben wurde). Die Unterbereiche werden ignoriert, und das gesamte Bild wird mit denselben Einstellungen gefiltert. Es gibt mehrere Gründe, warum eine Anwendung dies tun würde.

1.  Die Anwendung unterstützt möglicherweise nicht das Ändern der Einstellungen (z. b. durch [**WIA- \_ IPS- \_ Helligkeit**](-wia-wiaitempropscanneritem.md) und **WIA- \_ IPS \_**) für jede Region, die der Segmentierungs Filter erkennt (oder der Segmentierungs Filter kann nicht einmal verwendet werden). Es ist einfacher, dass die Anwendung **iwiapreview:: updatepreview** mit **wiapreviewreturnoriginalimage** aufruft, damit Sie immer das vollständige Image aus der WIA 2,0 Preview-Komponente empfängt.
2.  Die WIA 2,0 Preview-Komponente unterstützt das Bildformat des Vorschaubilds nicht. in diesem Fall können die Aktionen nicht zum Ausschneiden der gewünschten Region durchgeführt werden. Die Unterstützung von Image Formaten der WIA 2,0 Preview-Komponente ist auf Formate beschränkt, für die Windows GDI+ 1,1 Encoder und Decoders vorhanden sind. Diese Formate sind Bitmap (BMP) (eine Bitmap, die den BITMAPFILEHEADER enthält), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) und Tagged Image File Format (TIFF).

Beachten Sie Folgendes: Wenn die Anwendung **wiapreviewreturnoriginalimage** an **iwiapreview:: updatepreview** übergibt, kann die WIA 2,0-Vorschau Komponente jedes beliebige Bild oder Pixel Format unterstützen.

**Iwiapreview:: updatepreview** legt die [**WIA-Eigenschaft \_ DPS \_ Preview**](-wia-wiaitempropscannerdevice.md) fest (und setzt Sie vor der Rückgabe zurück, es sei denn, Sie wurde zuvor festgelegt). Dadurch kann der Treiber (und die Hardware) und der Bild Verarbeitungs Filter wissen, dass es sich bei dem Element um eine Vorschauversion handelt.

Eine Anwendung muss sicherstellen, dass *pchildwiaitem* über das gleiche Bildformat ([**WIA \_ IPA- \_ Format**](-wia-wiaitempropcommonitem.md)) und die Auflösung ([**WIA- \_ IPS \_ xres**](-wia-wiaitempropscanneritem.md) und **WIA- \_ IPS \_**) wie *pwiaitem* verfügt, als es an [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md)übergeben wurde. Das Format des untergeordneten Elements muss dem Format des zwischengespeicherten Images der WIA 2,0-Vorschau Komponente entsprechen (die WIA 2,0 Preview-Komponente führt keine Bild Konvertierung aus).

## <a name="examples"></a>Beispiele

Updateregion sollte jedes Mal aufgerufen werden, wenn sich ein Benutzer ändert, z. b. die Helligkeit oder der Kontrast für das untergeordnete Element, das durch dargestellt wird `dwRegionNumber` . Dieses untergeordnete Element wurde zuvor vom Segmentierungs Filter ([**iwiasegmentationfilter**](-wia-iwiasegmentationfilter.md)) erstellt. Das in [IStream](/windows/win32/api/objidl/nn-objidl-istream) geschriebene Bild wird von der [**getnextstream**](-wia-iwiatransfercallback-getnextstream.md) -Methode der Übertragungs Rückruf Schnittstelle zurückgegeben. Der Code für "getsubregionitem" wird in diesem Beispiel ausgelassen.

Nachdem diese Funktion aufgerufen wurde, würde eine Anwendung in der Regel den Bereich auf dem Bildschirm neu zeichnen.


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
