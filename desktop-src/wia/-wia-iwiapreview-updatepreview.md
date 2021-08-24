---
description: Ruft das ungefilterte Bild ab, das von der IWiaPreview::GetNewPreview-Methode zwischengespeichert wird.
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: IWiaPreview::UpdatePreview-Methode (Wia.h)
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
ms.openlocfilehash: b5f48462d926d96acebf4a74f0a843d82f9cd97190585b954565d5da649ff9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549690"
---
# <a name="iwiapreviewupdatepreview-method"></a>IWiaPreview::UpdatePreview-Methode

Ruft das ungefilterte Bild ab, das von der [**IWiaPreview::GetNewPreview-Methode zwischengespeichert**](-wia-iwiapreview-getnewpreview.md) wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lOptions* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt an, ob für die Anwendung die WIA 2.0 Preview-Komponente eine Unterregion des zwischengespeicherten Bilds oder das gesamte zwischengespeicherte Bild an den Bildverarbeitungsfilter übergeben muss.

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**


</dt> <dd>

Übergeben Sie das gesamte zwischengespeicherte Bild an den Bildverarbeitungsfilter.

</dd> </dl> </dd> <dt>

*pChildWiaItem* \[ In\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Gibt einen Zeiger auf das [**IWiaItem2-Element**](-wia-iwiaitem2.md) an, das ein untergeordnetes Element des **IWiaItem2-Elements** ist, das durch den *pWiaItem2-Parameter* der [**IWiaPreview::GetNewPreview-Methode**](-wia-iwiapreview-getnewpreview.md) angegeben wird. Wenn die Anwendung eine Vorschau des gesamten Flatbeds erfordert, gibt einen Zeiger auf den *pWiaItem2-Parameter* der **IWiaPreview::GetNewPreview-Methode** an. Wenn *pChildWiaItem* ein untergeordnetes Element des *pWiaItem2-Parameters* von **IWiaPreview::GetNewPreview** ist, wird dieses untergeordnete Element in der Regel durch den Segmentierungsfilter erstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode übergibt das zwischengespeicherte, ungefilterte Bild über den Bildverarbeitungsfilter, der die gefilterten Daten dann in den von der Anwendung bereitgestellten Stream schreibt. Die WIA 2.0 Preview-Komponente ruft diesen Stream ab, indem sie die [**GetNextStream-Methode**](-wia-iwiatransfercallback-getnextstream.md) des Bildverarbeitungsfilters aufruft, die dann die **GetNextStream-Implementierung** des Anwendungsrückrufs aufruft. Vor dem **Aufrufen von IWiaPreview::UpdatePreview** muss eine Anwendung zuerst [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) aufrufen, um das Bild vom Scanner zu erhalten. andernfalls gibt die Methode einen Fehler zurück.

Die WIA 2.0 Preview-Komponente speichert das ungefilterte Image, das vom Treiber heruntergeladen wurde. Es ist möglich, dass das an **IWiaPreview::UpdatePreview** übergebene WIA 2.0-Element nur einen kleinen Bereich des images darstellt, das vom Treiber heruntergeladen wurde. Wenn dies der Fall ist, schneidet die WIA 2.0 Preview-Komponente diesen Bereich tatsächlich aus dem zwischengespeicherten Bild ab, bevor sie es an den Bildverarbeitungsfilter übergibt, der wiederum die gefilterten Bilddaten an die Anwendung übergibt.

Damit eine Anwendung das gesamte zwischengespeicherte Bild an den Bildverarbeitungsfilter übergibt (der es wiederum an die Anwendung übergibt), muss sie beim Aufrufen von **IWiaPreview::UpdatePreview** die *lOptions* auf **WiaPreviewReturnOriginalImage** festlegen. Wenn *lOptions* auf **WiaPreviewReturnOriginalImage** festgelegt wird, muss die Anwendung sicherstellen, dass die Blockeinstellungen ([**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md) und **WIA \_ IPS \_ YEXTENT)** des elements, das an **IWiaPreview::UpdatePreview** übergeben wird, mit dem vollständig zwischengespeicherten Image übereinstimmungen. Der Bildverarbeitungsfilter muss in diesem Fall nichts anderes tun. Es filtert einfach das Bild basierend auf den Eigenschaften von *pChildWiaItem* (in der Regel ist *pChildWiaItem* dasselbe Element, das an [**IWiaPreview::GetNewPreview übergeben**](-wia-iwiapreview-getnewpreview.md)wurde). Die verschiedenen Unterregionen werden ignoriert, und das gesamte Bild wird mit den gleichen Einstellungen gefiltert. Es gibt mehrere Gründe, warum eine Anwendung dies tun würde.

1.  Die Anwendung unterstützt möglicherweise nicht, die Einstellungen (wie [**WIA \_ IPS \_ BRIGHTNESS**](-wia-wiaitempropscanneritem.md) und **WIA \_ IPS \_ CONTRAST)** einzeln für jede Region zu ändern, die der Segmentierungsfilter erkennt (oder möglicherweise nicht einmal den Segmentierungsfilter verwenden möchte). Es ist einfacher, dass die Anwendung **IWiaPreview::UpdatePreview** mit **WiaPreviewReturnOriginalImage** aufruft, sodass sie immer das vollständige Image von der WIA 2.0 Preview-Komponente empfängt.
2.  Die WIA 2.0 Preview-Komponente unterstützt das Bildformat des Vorschaubilds nicht. In diesem Fall kann sie die Aktionen zum Ausschneiden des gewünschten Bereich nicht ausführen. Die Bildformatunterstützung der WIA 2.0 Preview-Komponente ist auf Formate beschränkt, für die es Windows GDI+ 1.1-Encoder und -Decoder gibt. Diese Formate sind Bitmap (BMP) (eine Bitmap, die BITMAPFILEHEADER enthält), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) und Tagged Image File Format (TIFF).

Beachten Sie: Wenn die Anwendung **WiaPreviewReturnOriginalImage** an **IWiaPreview::UpdatePreview** übergibt, kann die WIA 2.0 Preview-Komponente jedes Bild- oder Pixelformat unterstützen.

**IWiaPreview::UpdatePreview** legt die [**WIA \_ DPS \_ PREVIEW-Eigenschaft**](-wia-wiaitempropscannerdevice.md) fest (und setzt sie zurück, bevor sie zurückgegeben wird, es sei denn, sie wurde zuvor festgelegt). Dadurch können der Treiber (und die Hardware) sowie der Bildverarbeitungsfilter wissen, dass es sich bei dem Element um eine Vorschauprüfung handelt.

Eine Anwendung muss sicherstellen, dass *pChildWiaItem* das gleiche Bildformat ([**WIA \_ IPA \_ FORMAT**](-wia-wiaitempropcommonitem.md)) und die gleiche Auflösung ([**WIA \_ IPS \_ XRES**](-wia-wiaitempropscanneritem.md) und **WIA \_ IPS \_ YRES**) wie *pWiaItem* hat, als es an [**IWiaPreview::GetNewPreview übergeben wurde.**](-wia-iwiapreview-getnewpreview.md) Das Format des untergeordneten Elements muss dem Format des zwischengespeicherten Images der WIA 2.0 Preview-Komponente entsprechen (die WIA 2.0 Preview-Komponente führt keine Bildkonvertierung durch).

## <a name="examples"></a>Beispiele

UpdateRegion sollte jedes Mal aufgerufen werden, wenn sich ein Benutzer ändert, z. B. die Helligkeit oder den Kontrast für das untergeordnete Element, das durch dargestellt `dwRegionNumber` wird. Dieses untergeordnete Element wurde zuvor vom Segmentierungsfilter ([**IWiaSegmentationFilter ) erstellt.**](-wia-iwiasegmentationfilter.md) Das in den [IStream geschriebene Bild](/windows/win32/api/objidl/nn-objidl-istream) wird von der [**GetNextStream-Methode der Übertragungsrückrufschnittstelle**](-wia-iwiatransfercallback-getnextstream.md) zurückgegeben. Der Code für GetSubRegionItem wird in diesem Beispiel ausgelassen.

Nachdem diese Funktion aufgerufen wurde, wird der Bereich in der Regel von einer Anwendung auf dem Bildschirm neu gezeichnet.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
