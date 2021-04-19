---
description: Implementieren von IWICBitmapCodecProgressNotification (Decoder)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementieren von IWICBitmapCodecProgressNotification (Decoder)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362513"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a>Implementieren von IWICBitmapCodecProgressNotification (Decoder)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Wenn ein Codec einen e/a-Vorgang ausführt, z. b. [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) in einem großen Bild, kann es mehrere Sekunden oder sogar Minuten dauern. Wenn Endbenutzer einen Vorgang mit langer Ausführungszeit nicht unterbrechen können, kann die Anwendung davon ausgehen, dass die Anwendung nicht reagiert hat. Benutzer werden häufig eine Anwendung schließen oder sogar Ihre Computer neu starten, um die Kontrolle über den Computer wiederherzustellen, wenn eine Anwendung nicht mehr reagiert.

Diese Schnittstelle ermöglicht es einer Anwendung, eine Rückruffunktion anzugeben, die der Codec in angegebenen Intervallen aufzurufen kann, um den Aufrufer über den Fortschritt des aktuellen Vorgangs zu benachrichtigen. Die Anwendung kann mithilfe dieser Rückruffunktion einen Hinweis auf den Fortschritt in der Benutzeroberfläche anzeigen, um den Benutzer über den Status des Vorgangs zu benachrichtigen. Wenn ein **Benutzer im Status Dialogfeld** auf die Schaltfläche **Abbrechen** klickt, gibt die Anwendung den von der Rückruffunktion **\_ \_ abgebrochenen wincodec Err** zurück. Wenn dies der Fall ist, muss der Codec den angegebenen Vorgang abbrechen und dieses **HRESULT** zurück an den Aufrufer der Methode übergeben, die den Vorgang durchgeführt hat.

Diese Schnittstelle sollte in Ihrer Decoder-Klasse auf Container-Ebene implementiert werden.


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
-   [PfnProgressNotification](#pfnprogressnotification)

### <a name="registerprogressnotification"></a>RegisterProgressNotification

[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) wird von einer Anwendung aufgerufen, um eine Rückruffunktion zu registrieren, die der Codec in angegebenen Intervallen aufrufen kann. Der erste Parameter, *pfnProgressNotification*, ist ein Zeiger auf die Rückruffunktion, die der Codec in regelmäßigen Abständen aufrufen sollte.

Der *pvData* -Parameter verweist auf ein Objekt, das der Codec an die Rückruffunktion zurückgeben soll, wenn die Rückruffunktion aufgerufen wird. Dieses Objekt kann überhaupt alles sein und hat keine besondere Bedeutung für den Codec.

Der *dwprogressflags* -Parameter gibt an, wann der Codec die Rückruffunktion aufrufen soll. Eine-oder-Funktion kann mit zwei Enumerationen für diesen Parameter ausgeführt werden. Die [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) -Enumeration gibt an, ob die Rückruffunktion während der Decodierung (**WICProgressOperationCopyPixels**), Codierung (**wicprogerssoperationschreitepixel**) oder beides (**WICProgressOperationAll**) aufgerufen werden soll.


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



Der Codec sollte die Rückruffunktion in regelmäßigen Abständen während des Vorgangs aufzurufen, aber der Aufrufer kann bestimmte Anforderungen angeben. Die [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) -Enumeration gibt an, an welchem Punkt des Vorgangs die Rückruffunktion aufgerufen werden soll. Wenn der Aufrufer **WICProgressNotificationBegin** angibt, muss er am Anfang des Vorgangs (0,0) aufgerufen werden. Wenn der Aufrufer diese Angabe nicht angibt, ist er optional. Wenn der Aufrufer **wicprogerssnotificationend** angibt, müssen Sie ihn ebenso angeben, wenn der Vorgang abgeschlossen ist (1,0). Wenn der Aufrufer **WICProgressNotificationAll** angibt, müssen Sie ihn am Anfang und am Ende sowie in regelmäßigen Abständen während des Vorgangs ausführen. Der Aufrufer kann auch **wicprogerssnotificationfrequent** angeben. Dies deutet darauf hin, dass Sie in regelmäßigen Abständen (möglicherweise nach jedem Paar Scan Zeilen) wieder aufgerufen werden möchten. (Ein Aufrufer verwendet dieses Flag in der Regel nur für ein sehr großes Bild.) Andernfalls sollten Sie in der Regel einen Rückruf in Intervallen von ungefähr 10 Prozent der Gesamtzahl der zu verarbeitenden Scan Zeilen durchgehen.


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



Für einen bestimmten Decoder oder eine Encoder-Instanz kann jeweils nur eine Rückruffunktion registriert werden. Wenn eine Anwendung [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) mehrmals aufruft, ersetzen Sie die zuvor registrierte Rückruffunktion durch die neue. Um eine Rückruf Registrierung abzubrechen, legt ein Aufrufer den *pfnProgressNotification* -Parameter auf **null** fest.

### <a name="pfnprogressnotification"></a>PfnProgressNotification

[**PfnProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) ist die Rückruffunktion mit der folgenden Signatur.


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



Wenn Sie die Rückruffunktion aufrufen, verwenden Sie den *pvData* -Parameter, um dieselben *pvData* zurückzugeben, die von der Anwendung beim Registrieren der Rückruffunktion angegeben wurden.

Der *uFrameNum* -Parameter sollte den Index des Frame angeben, der verarbeitet wird.

Legen Sie den Vorgangs Parameter auf **WICProgressOperationCopyPixels** fest, wenn Sie decodieren und **wicprogressoperationwrite tepixel** bei der Codierung verwenden.

Der *dblProgress* -Parameter muss eine Zahl zwischen 0,0 (Beginn des Vorgangs) und 1,0 (der Abschluss des Vorgangs) sein. Der Wert sollte den Anteil der bereits verarbeiteten Scan Zeilen im Verhältnis zur Gesamtzahl der zu verarbeitenden Scan Zeilen widerspiegeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Progressnotificationcallback**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

**Licher**
</dt> <dt>

[Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Implementieren von IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



