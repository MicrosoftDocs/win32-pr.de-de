---
description: Implementieren von IWICBitmapCodecProgressNotification (Decoder)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementieren von IWICBitmapCodecProgressNotification (Decoder)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff9af6bbd8c0457a5bf97f2f8b378cdeaca9269e792f7ed4696ab8e6a23b89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088062"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a>Implementieren von IWICBitmapCodecProgressNotification (Decoder)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Wenn ein Codec einen E/A-Vorgang wie [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) für ein großes Bild ausführt, kann es einige Sekunden oder sogar Minuten dauern, bis er abgeschlossen ist. Wenn Endbenutzer einen zeitintensiven Vorgang nicht unterbrechen können, könnten sie denken, dass die Anwendung hängen geblieben ist. Benutzer schließen häufig eine Anwendung oder starten sogar ihre Computer neu, um die Kontrolle über ihren Computer zurückzuerlangen, wenn eine Anwendung nicht mehr reagiert.

Mit dieser Schnittstelle kann eine Anwendung eine Rückruffunktion angeben, die der Codec in angegebenen Intervallen aufrufen kann, um den Aufrufer über den Fortschritt des aktuellen Vorgangs zu benachrichtigen. Die Anwendung kann diese Rückruffunktion verwenden, um einen Hinweis auf den Fortschritt auf der Benutzeroberfläche anzuzeigen, um den Benutzer über den Status des Vorgangs zu benachrichtigen. Wenn ein Benutzer im Dialogfeld **Status** auf die Schaltfläche **Abbrechen** klickt, gibt die Anwendung **WINCODEC \_ ERR \_ ABORTED** von der Rückruffunktion zurück. In diesem Fall muss der Codec den angegebenen Vorgang abbrechen und dieses **HRESULT** an den Aufrufer der Methode zurückgeben, die den Vorgang ausgeführt hat.

Diese Schnittstelle sollte für Ihre Decoderklasse auf Containerebene implementiert werden.


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [RegisterProgressNotification](#registerprogressnotification)
-   [PFNProgressNotification](#pfnprogressnotification)

### <a name="registerprogressnotification"></a>RegisterProgressNotification

[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) wird von einer Anwendung aufgerufen, um eine Rückruffunktion zu registrieren, die der Codec in angegebenen Intervallen aufrufen kann. Der erste Parameter, *pfnProgressNotification,* ist ein Zeiger auf die Rückruffunktion, die der Codec in regelmäßigen Abständen aufrufen soll.

Der *pvData-Parameter* verweist auf ein Objekt, das der Aufrufer vom Codec an die Rückruffunktion zurückgeben soll, wenn die Rückruffunktion aufgerufen wird. Dieses Objekt kann überhaupt etwas sein und hat keine besondere Bedeutung für den Codec.

Der *dwProgressFlags-Parameter* gibt an, wann der Codec die Rückruffunktion aufrufen soll. Eine OR-Funktion kann mit zwei Enumerationen für diesen Parameter ausgeführt werden. Die [**WICProgressOperation-Enumeration**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) gibt an, ob die Rückruffunktion während der Decodierung (**WICProgressOperationCopyPixels),** Codierung (**WICProgerssOperationWritePixels**) oder beides (**WICProgressOperationAll**) aufgerufen werden soll.


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



Der Codec sollte die Rückruffunktion in regelmäßigen Abständen während des gesamten Vorgangs aufrufen, aber der Aufrufer kann bestimmte Anforderungen angeben. Die [**WICProgressNotification-Enumeration**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) gibt an, an welchem Punkt des Vorgangs die Rückruffunktion aufgerufen werden soll. Wenn der Aufrufer **WICProgressNotificationBegin** angibt, müssen Sie ihn zu Beginn des Vorgangs (0.0) aufrufen. Wenn der Aufrufer dies nicht angibt, ist dies optional. Wenn der Aufrufer **WICProgerssNotificationEnd** angibt, müssen Sie ihn nach Abschluss des Vorgangs aufrufen (1.0). Wenn der Aufrufer **WICProgressNotificationAll** angibt, müssen Sie ihn am Anfang und Ende sowie in regelmäßigen Intervallen während des gesamten Vorgangs aufrufen. Der Aufrufer kann auch **WICProgerssNotificationFrequent** angeben, was darauf hinweist, dass er in regelmäßigen Intervallen , möglicherweise nach jedem Paar von Scanzeilen, zurückgerufen werden soll. (Ein Aufrufer verwendet dieses Flag in der Regel nur für ein sehr großes Image.) Andernfalls sollten Sie in der Regel einen Rückruf in Intervallen von etwa 10 Prozent der Gesamtzahl der zu verarbeitenden Scanzeilen durchführen.


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



Für einen bestimmten Decoder oder eine Encoderinstanz kann jeweils nur eine Rückruffunktion registriert werden. Wenn eine Anwendung [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) mehr als einmal aufruft, ersetzen Sie die zuvor registrierte Rückruffunktion durch die neue. Um eine Rückrufregistrierung abzubrechen, legt ein Aufrufer den *pfnProgressNotification-Parameter* auf **NULL** fest.

### <a name="pfnprogressnotification"></a>PFNProgressNotification

[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) ist die Rückruffunktion mit der folgenden Signatur.


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



Wenn Sie die Rückruffunktion aufrufen, verwenden Sie den *parameter pvData,* um die gleichen *pvData-Daten* zurückzugeben, die die Anwendung beim Registrieren der Rückruffunktion angegeben hat.

Der *uFrameNum-Parameter* sollte den Index des Frames angeben, der verarbeitet wird.

Legen Sie den Vorgangsparameter beim Decodieren auf **WICProgressOperationCopyPixels** und bei der Codierung **auf WICProgressOperationWritePixels** fest.

Der *dblProgress-Parameter* sollte eine Zahl zwischen 0,0 (dem Anfang des Vorgangs) und 1,0 (dem Abschluss des Vorgangs) sein. Der Wert sollte den Anteil der bereits verarbeiteten Scanzeilen relativ zur Gesamtzahl der zu verarbeitenden Scanzeilen widerspiegeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**ProgressNotificationCallback**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Implementieren von IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



