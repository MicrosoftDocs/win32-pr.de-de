---
title: WIC-Funktionen
description: Dieser Abschnitt enthält Informationen zu den Windows Imaging Component (WIC)-Funktionen.
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f60660780e97831a77101c15646385d62048f005279b388a532ca687a200996
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056800"
---
# <a name="wic-functions"></a>WIC-Funktionen

Dieser Abschnitt enthält Informationen zu den Windows Imaging Component (WIC)-Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                      | BESCHREIBUNG                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*ProgressNotificationCallback*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | Die von der Anwendung definierte Rückruffunktion wird aufgerufen, wenn der Fortschritt der Codeckomponente erfolgt.<br/>                                                                                                                        |
| [**WICConvertBitmapSource**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | Erhält eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) im gewünschten Pixelformat aus einer **angegebenen IWICBitmapSource.**<br/>                                                                           |
| [**WICCreateBitmapFromSection**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | Gibt eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) zurück, die durch die Pixel eines GDI-Windows Graphics Device Interface (GDI) unterstützt wird.<br/>                                                |
| [**WICCreateBitmapFromSectionEx**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | Gibt eine [**IWICBitmapSource zurück,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) die durch die Pixel eines GDI-Abschnittshandpunkts unterstützt wird.<br/>                                                                                    |
| [**WICGetMetadataContentSize**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | Gibt die Größe des Metadateninhalts zurück, der im angegebenen [**IWICMetadataWriter enthalten ist.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) Die zurückgegebene Größe gibt den Header und die Länge der Metadaten an.<br/> |
| [**WICMapGuidToShortName**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | Erhält den Kurznamen, der einer angegebenen GUID zugeordnet ist.<br/>                                                                                                                                                       |
| [**WICMapSchemaToName**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | Erhält den Namen, der einem angegebenen Schema zugeordnet ist.<br/>                                                                                                                                                           |
| [**WICMapShortNameToGuid**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | Erhält die GUID, die dem angegebenen Kurznamen zugeordnet ist.<br/>                                                                                                                                                     |
| [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | Erhält eine METADATENformat-GUID für ein angegebenes Containerformat und einen Anbieter, der am besten mit dem Inhalt innerhalb eines bestimmten Streams abordnt.<br/>                                                                            |
| [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | Schreibt Metadaten in einen bestimmten Stream.<br/>                                                                                                                                                                       |
| [WIC-Proxyfunktionen](wic-proxy-functions.md)<br/>                                  | Dieser Abschnitt enthält die WIC-Proxyfunktionen.<br/>                                                                                                                                                             |



 

 

 




