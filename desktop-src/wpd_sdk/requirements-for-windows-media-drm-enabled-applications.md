---
description: Anforderungen für Windows Media DRM-Enabled Anwendungen
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Anforderungen für Windows Media DRM-Enabled Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ad59b5b590436ca5734fcb8d226d41f4f995a5d4ea97e0c46d771df476be6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027049"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Anforderungen für Windows Media DRM-Enabled Anwendungen

Um eine Windows Media Digital Rights Management(DRM)-fähige Anwendung zu erstellen, müssen Sie über die [](general-requirements-for-application-development.md) Header und Bibliotheken verfügen, die im Abschnitt Allgemeine Anforderungen für die Anwendungsentwicklung dieses Dokuments beschrieben sind. Darüber hinaus muss die Anwendung beim Öffnen des Geräts zusätzliche Eigenschaften in den Clientinformationen enthalten.

Die beiden zusätzlichen Eigenschaften, die zum Aktivieren Windows Medien-DRM-geschützten Inhaltsübertragungen erforderlich sind, werden in der folgenden Tabelle beschrieben.



| Eigenschaft                                      | Beschreibung                              |
|-----------------------------------------------|------------------------------------------|
| WPD \_ CLIENT \_ WMDRM \_ APPLICATION \_ PRIVATE \_ KEY | Gibt den privaten Schlüssel der Anwendung an. |
| \_ \_ WPD-CLIENT-WMDRM-ANWENDUNGSZERTIFIKAT \_ \_  | Gibt das Zertifikat der Anwendung an. |



 

Diese Eigenschaften müssen in den Clientinformationen der Anwendung angegeben werden, wenn das Gerät mit der [**IPortableDevice::Open-Methode geöffnet**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) wird. Wenn diese Eigenschaften bereitgestellt werden, lässt die WPD-API übertragungen geschützter Inhalte zu. Wenn die Anwendung ein Zertifikat und einen privaten Schlüssel bereitgestellt hat, erstellt die API einen sicheren Kanal zum Übertragen geschützter WMDRM-Inhalte auf das Gerät.

Informationen zum Erstellen und Verteilen von Windows-basierten Anwendungen, die Windows Media DRM unterstützen, finden Sie im folgenden Thema Licensing Windows-based Applications (Lizenzierung [Windows-basierten](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) Anwendungen).

## <a name="transferring-content"></a>Übertragen von Inhalten

Verwenden Sie zum Übertragen von durch WMDRM geschützten Inhalt [**IPortableDeviceContent::CreateObjectWithPropertiesAndData.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) Diese Methode kann sowohl für geschützten als auch für löschenden Inhalt ohne zusätzliche Optionen verwendet werden. Die WPD-API wählt automatisch den geschützten oder gelöschten Kanal aus, je nachdem, ob der Inhalt geschützt oder klar ist. Er ist mit dem WMDRM Secure Content Provider verbunden, um die WMDRM-Lizenzen zu verarbeiten.

## <a name="transferring-known-clear-content"></a>Übertragen von bekannten eindeutigen Inhalten

Wenn Sie Ihre Anwendung für die Verarbeitung geschützter Inhalte aktiviert haben, aber wissen, dass eine bestimmte Datei nicht geschützt ist, können Sie WPD anraten, die DRM-Verarbeitung zu überspringen, indem Sie die **\_ WPD-API-Option \_ USE CLEAR \_ DATA \_ \_ \_ STREAM** in der **Eingabe IPortableDeviceValues** auf TRUE festlegen, wenn [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) für eindeutigen Inhalt aufruft.

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Zugreifen auf Messungsvorgänge mithilfe von IWMDRMDeviceApp

WPD bietet einen Mechanismus für den Zugriff auf **die IWMDRMDeviceApp-APIs** für Lizenzupdates und den Abruf von Messungsdaten. Um über WPD auf diese API zuzugreifen, rufen Sie **QueryInterface** in **IID \_ IWMDRMDeviceApp** aus dem von [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)zurückgegebenen **IStream** auf. Diese **IWMDRMDeviceApp-Instanz** ist an die **IPortableDevice-Verbindung** mit Ihrem WMDRM-kompatiblen Gerät gebunden und nicht an den spezifischen Inhalt, an dem **der IStream** erhalten wurde. WPD umschließt die Messungs-APIs intern und macht sie für Ihre Anwendung zugänglich. Ihre Anwendung sollte die WMDRMDEVICEAPP USE WPD DEVICE PTR-Konstante für den \_ \_ \_ \_ *IWMDMDevice-Parameter* \* verwenden.

Dies wird im folgenden Codeausschnitt veranschaulicht.


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



Die gleiche Voraussetzung wie für den privaten Schlüssel und das Zertifikat der Anwendung gilt auch hier. Wenn der Schlüssel/das Zertifikat ungültig ist oder das WMDRM-System nicht initialisiert werden kann, schlägt der **QueryInferface-Aufruf** fehl.

Die oben beschriebene Methode zum Erwerben der **IWMDRMDeviceApp-Schnittstelle** aus dem **IStream-Zeiger** ist nur eine Vereinfachung, wenn Ihre Anwendung bereits eine vorherige Übertragung geschützter Inhalte vor der Vermessung und Lizenzsynchronisierung vor dem Durchführen von Messungs- und Lizenzsynchronisierungsvorgängen durchläuft.

Für die meisten Anwendungen, die auf **IWMDRMDeviceApp** zugreifen müssen, wird empfohlen, **IWMDRMDeviceApp** direkt zu initialisieren, da ihre Anwendung dafür weder geschützte Inhalte übertragen noch an die Übertragungsschnittstellen halten muss, um Gerätemessung und Lizenzsynchronisierung zu ermöglichen. Diese Methode erfordert die Verwendung von Windows Media Geräte-Manager-APIs (WMDM). Details und Beispielcode finden Sie im Whitepaper [Accessing WMDRM APIs from a WPD Application (Zugreifen auf WMDRM-APIs](../windows-portable-devices.md) aus einer WPD-Anwendung) auf der WHDC-Website.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Portable Geräte**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
