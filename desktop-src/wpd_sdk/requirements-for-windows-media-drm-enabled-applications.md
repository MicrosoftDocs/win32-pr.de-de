---
description: Anforderungen für Windows Media DRM-Enabled-Anwendungen
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Anforderungen für Windows Media DRM-Enabled-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353258"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Anforderungen für Windows Media DRM-Enabled-Anwendungen

Zum Erstellen einer Windows Media Digital Rights Management (DRM)-fähigen Anwendung benötigen Sie die Header und Bibliotheken, die im Abschnitt [Allgemeine Anforderungen für die Anwendungsentwicklung](general-requirements-for-application-development.md) in diesem Dokument beschrieben werden. Außerdem muss die Anwendung beim Öffnen des Geräts zusätzliche Eigenschaften in den Client Informationen bereitstellen.

In der folgenden Tabelle werden die beiden zusätzlichen Eigenschaften, die zum Aktivieren von Windows Media DRM-geschützten Inhalts Übertragungen erforderlich sind, beschrieben.



| Eigenschaft                                      | BESCHREIBUNG                              |
|-----------------------------------------------|------------------------------------------|
| privater Schlüssel für WPD- \_ Client \_ WMDRM- \_ Anwendung \_ \_ | Gibt den privaten Schlüssel der Anwendung an. |
| WPD- \_ Client- \_ WMDRM- \_ Anwendungs \_ Zertifikat  | Gibt das Zertifikat der Anwendung an. |



 

Diese Eigenschaften müssen in den Client Informationen der Anwendung angegeben werden, wenn das Gerät mit der [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) -Methode geöffnet wird. Wenn diese Eigenschaften angegeben werden, ermöglicht die WPD-API die Übertragung geschützter Inhalte. Wenn die Anwendung ein Zertifikat und einen privaten Schlüssel bereitgestellt hat, erstellt die API einen sicheren Kanal für die Übertragung geschützter WMDRM-Inhalte auf das Gerät.

Informationen zum Erstellen und Verteilen von Windows-basierten Anwendungen, die Windows Media DRM unterstützen, finden Sie im Thema zur [Lizenzierung Windows-basierter Anwendungen](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .

## <a name="transferring-content"></a>Inhalt wird übertragen

Verwenden Sie zum Übertragen von WMDRM-geschütztem Inhalt [**iportabledevicecontent:: |-objectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Diese Methode kann sowohl für den geschützten als auch für den Lösch Inhalt ohne zusätzliche Optionen verwendet werden. Abhängig davon, ob der Inhalt geschützt oder gelöscht wird, wählt die WPD-API automatisch den geschützten oder leeren Kanal aus. Es wird mit dem WMDRM-Anbieter für sichere Inhalte zum Verarbeiten der WMDRM-Lizenzen über eine Schnittstelle.

## <a name="transferring-known-clear-content"></a>Übertragen von bekanntem Klartext

Wenn Sie Ihre Anwendung für die Handhabung geschützter Inhalte aktiviert haben, wenn Sie jedoch wissen, dass eine bestimmte Datei nicht geschützt ist, können Sie WPD anweisen, die DRM-Verarbeitung zu überspringen, indem Sie die **\_ Option " \_ \_ \_ Clear \_ Data \_ Stream verwenden** " in der Eingabe " **iportabledevicevalues** " festlegen, wenn Sie " [**iportabledevicecontent:: createobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) " für den Inhalt löschen

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Zugreifen auf Messungs Vorgänge mithilfe von iwmdrmdeviceapp

WPD bietet einen Mechanismus für den Zugriff auf die **iwmdrmdeviceapp** -APIs, um Lizenz Updates und den Abruf von Messungs Daten zu erhalten. Um über WPD auf diese API zuzugreifen, aufrufen Sie **QueryInterface** für **IID \_ iwmdrmdeviceapp** aus dem **IStream** , der von [**iportabledevicecontent:: deateobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)zurückgegeben wurde. Diese **iwmdrmdeviceapp** -Instanz ist an die **iportabledevice** -Verbindung mit dem WMDRM-kompatiblen Gerät gebunden, nicht an dem spezifischen Inhalt, in dem der **IStream** abgerufen wurde. WPD umschließt die Messungs-APIs intern und macht Sie für Ihre Anwendung zugänglich. Die Anwendung sollte die \_ \_ ptr-Konstante WPD- \_ Gerät \_ für den *iwmdmdevice* - \* Parameter verwenden.

Dies wird im folgenden Code Ausschnitt veranschaulicht.


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



Diese Voraussetzung gilt auch für den privaten Schlüssel der Anwendung und das Zertifikat. Wenn der Schlüssel/das Zertifikat ungültig ist oder das WMDRM-System nicht initialisiert werden kann, schlägt der **queryinferface** -Rückruf fehl.

Die obige Methode zum Abrufen der **iwmdrmdeviceapp** -Schnittstelle über den **IStream** -Zeiger ist nur eine einfache Möglichkeit, wenn Ihre Anwendung bereits eine zuvor geschützte Inhalts Übertragung durchführen muss, bevor Sie mit der Verarbeitung von Messungs-und Lizenz Synchronisierungs Vorgängen fortfahren.

Die Empfehlung für die meisten Anwendungen, die auf **iwmdrmdeviceapp** zugreifen müssen, besteht darin, **iwmdrmdeviceapp** direkt zu initialisieren, da es nicht erforderlich ist, dass Ihre Anwendung geschützte Inhalte überträgt oder an den Übertragungs Schnittstellen hält, um die Geräte Messung und die Lizenz Synchronisierung durchzuführen. Diese Methode erfordert die Verwendung von WMDM-APIs (Windows Media Device Manager). Ausführliche Informationen und Beispielcode finden Sie im Whitepaper [zugreifen auf WMDRM-APIs von einer WPD-Anwendung](../windows-portable-devices.md) auf der whdc-Website.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Tragbare Windows-Geräte**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
