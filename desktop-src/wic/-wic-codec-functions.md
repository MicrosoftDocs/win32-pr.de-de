---
title: WIC-Funktionen
description: Dieser Abschnitt enthält Informationen zu den Funktionen der Windows Imaging Component (WIC).
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ce53f51f439ab5d0a697c824a1d37db7fd755f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862479"
---
# <a name="wic-functions"></a>WIC-Funktionen

Dieser Abschnitt enthält Informationen zu den Funktionen der Windows Imaging Component (WIC).

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                      | BESCHREIBUNG                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Progressnotificationcallback*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | Anwendungs definierte Rückruffunktion, die aufgerufen wird, wenn der Status der Codec-Komponente erfolgt.<br/>                                                                                                                        |
| [**Wicconvertbitmapsource**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | Ruft eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) im gewünschten Pixel Format aus einer angegebenen **IWICBitmapSource** ab.<br/>                                                                           |
| [**Wickreatebitmapfromsection**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | Gibt eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) zurück, die durch die Pixel eines Abschnitts Handles eines Windows Graphics Device Interface (GDI) unterstützt wird.<br/>                                                |
| [**Wickreatebitmapfromsectionex**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | Gibt eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) zurück, die durch die Pixel eines GDI-Abschnitts Handles unterstützt wird.<br/>                                                                                    |
| [**WICGetMetadataContentSize**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | Gibt die Größe des metadateninhalts zurück, der im angegebenen [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)enthalten ist. Die zurückgegebene Größe berücksichtigt den Header und die Länge der Metadaten.<br/> |
| [**Wicmapguiddeshortname**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | Ruft den Kurznamen ab, der einer angegebenen GUID zugeordnet ist.<br/>                                                                                                                                                       |
| [**Wicmapschematoname**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | Ruft den einem angegebenen Schema zugeordneten Namen ab.<br/>                                                                                                                                                           |
| [**Wicmapshortnametoguid**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | Ruft die GUID ab, die dem angegebenen Kurznamen zugeordnet ist.<br/>                                                                                                                                                     |
| [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | Ruft eine GUID des metadatenformats für ein angegebenes Containerformat und einen Anbieter ab, die am besten mit dem Inhalt innerhalb eines angegebenen Streams übereinstimmt<br/>                                                                            |
| [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | Schreibt Metadaten in einen angegebenen Stream.<br/>                                                                                                                                                                       |
| [WIC-Proxy Funktionen](wic-proxy-functions.md)<br/>                                  | Dieser Abschnitt enthält die WIC-Proxy Funktionen.<br/>                                                                                                                                                             |



 

 

 




