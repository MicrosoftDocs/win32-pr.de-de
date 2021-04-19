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
# <a name="requirements-for-windows-media-drm-enabled-applications"></a><span data-ttu-id="fbe2b-103">Anforderungen für Windows Media DRM-Enabled-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="fbe2b-103">Requirements for Windows Media DRM-Enabled Applications</span></span>

<span data-ttu-id="fbe2b-104">Zum Erstellen einer Windows Media Digital Rights Management (DRM)-fähigen Anwendung benötigen Sie die Header und Bibliotheken, die im Abschnitt [Allgemeine Anforderungen für die Anwendungsentwicklung](general-requirements-for-application-development.md) in diesem Dokument beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-104">To create a Windows Media Digital Rights Management (DRM)-enabled application, you must have the headers and libraries described in the [General Requirements for Application Development](general-requirements-for-application-development.md) section of this document.</span></span> <span data-ttu-id="fbe2b-105">Außerdem muss die Anwendung beim Öffnen des Geräts zusätzliche Eigenschaften in den Client Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-105">In addition, the application will need to supply additional properties in the client information when opening the device.</span></span>

<span data-ttu-id="fbe2b-106">In der folgenden Tabelle werden die beiden zusätzlichen Eigenschaften, die zum Aktivieren von Windows Media DRM-geschützten Inhalts Übertragungen erforderlich sind, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-106">The two additional properties that are required to enable Windows Media DRM-protected content transfers are described in the following table.</span></span>



| <span data-ttu-id="fbe2b-107">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fbe2b-107">Property</span></span>                                      | <span data-ttu-id="fbe2b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbe2b-108">Description</span></span>                              |
|-----------------------------------------------|------------------------------------------|
| <span data-ttu-id="fbe2b-109">privater Schlüssel für WPD- \_ Client \_ WMDRM- \_ Anwendung \_ \_</span><span class="sxs-lookup"><span data-stu-id="fbe2b-109">WPD\_CLIENT\_WMDRM\_APPLICATION\_PRIVATE\_KEY</span></span> | <span data-ttu-id="fbe2b-110">Gibt den privaten Schlüssel der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-110">Specifies the application's private key.</span></span> |
| <span data-ttu-id="fbe2b-111">WPD- \_ Client- \_ WMDRM- \_ Anwendungs \_ Zertifikat</span><span class="sxs-lookup"><span data-stu-id="fbe2b-111">WPD\_CLIENT\_WMDRM\_APPLICATION\_CERTIFICATE</span></span>  | <span data-ttu-id="fbe2b-112">Gibt das Zertifikat der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-112">Specifies the application's certificate.</span></span> |



 

<span data-ttu-id="fbe2b-113">Diese Eigenschaften müssen in den Client Informationen der Anwendung angegeben werden, wenn das Gerät mit der [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) -Methode geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-113">These properties must be supplied in the application's client information when the device is opened with the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.</span></span> <span data-ttu-id="fbe2b-114">Wenn diese Eigenschaften angegeben werden, ermöglicht die WPD-API die Übertragung geschützter Inhalte.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-114">When these properties are supplied, the WPD API allows protected content transfers.</span></span> <span data-ttu-id="fbe2b-115">Wenn die Anwendung ein Zertifikat und einen privaten Schlüssel bereitgestellt hat, erstellt die API einen sicheren Kanal für die Übertragung geschützter WMDRM-Inhalte auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-115">If the application has provided a certificate and private key, the API will create a secure channel to transfer protected WMDRM content to the device.</span></span>

<span data-ttu-id="fbe2b-116">Informationen zum Erstellen und Verteilen von Windows-basierten Anwendungen, die Windows Media DRM unterstützen, finden Sie im Thema zur [Lizenzierung Windows-basierter Anwendungen](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fbe2b-116">For information about creating and distributing Windows-based applications that support Windows Media DRM, see the following [Licensing Windows-based Applications](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) topic.</span></span>

## <a name="transferring-content"></a><span data-ttu-id="fbe2b-117">Inhalt wird übertragen</span><span class="sxs-lookup"><span data-stu-id="fbe2b-117">Transferring Content</span></span>

<span data-ttu-id="fbe2b-118">Verwenden Sie zum Übertragen von WMDRM-geschütztem Inhalt [**iportabledevicecontent:: |-objectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="fbe2b-118">To transfer WMDRM protected content, use [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="fbe2b-119">Diese Methode kann sowohl für den geschützten als auch für den Lösch Inhalt ohne zusätzliche Optionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-119">This method can be used for both protected and clear content without additional options.</span></span> <span data-ttu-id="fbe2b-120">Abhängig davon, ob der Inhalt geschützt oder gelöscht wird, wählt die WPD-API automatisch den geschützten oder leeren Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-120">The WPD API will automatically select the protected or clear channel depending on whether the content is protected or clear.</span></span> <span data-ttu-id="fbe2b-121">Es wird mit dem WMDRM-Anbieter für sichere Inhalte zum Verarbeiten der WMDRM-Lizenzen über eine Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-121">It interfaces with the WMDRM Secure Content Provider to process the WMDRM licenses.</span></span>

## <a name="transferring-known-clear-content"></a><span data-ttu-id="fbe2b-122">Übertragen von bekanntem Klartext</span><span class="sxs-lookup"><span data-stu-id="fbe2b-122">Transferring Known Clear Content</span></span>

<span data-ttu-id="fbe2b-123">Wenn Sie Ihre Anwendung für die Handhabung geschützter Inhalte aktiviert haben, wenn Sie jedoch wissen, dass eine bestimmte Datei nicht geschützt ist, können Sie WPD anweisen, die DRM-Verarbeitung zu überspringen, indem Sie die **\_ Option " \_ \_ \_ Clear \_ Data \_ Stream verwenden** " in der Eingabe " **iportabledevicevalues** " festlegen, wenn Sie " [**iportabledevicecontent:: createobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) " für den Inhalt löschen</span><span class="sxs-lookup"><span data-stu-id="fbe2b-123">If you've enabled your application to handle protected content, but you know that a specific file is not protected, you can tell WPD to skip the DRM processing by setting **WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM** option to TRUE in the input **IPortableDeviceValues** when calling [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) for clear content.</span></span>

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a><span data-ttu-id="fbe2b-124">Zugreifen auf Messungs Vorgänge mithilfe von iwmdrmdeviceapp</span><span class="sxs-lookup"><span data-stu-id="fbe2b-124">Accessing Metering Operations using IWMDRMDeviceApp</span></span>

<span data-ttu-id="fbe2b-125">WPD bietet einen Mechanismus für den Zugriff auf die **iwmdrmdeviceapp** -APIs, um Lizenz Updates und den Abruf von Messungs Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-125">WPD provides a mechanism to access the **IWMDRMDeviceApp** APIs for license updates and metering data retrieval.</span></span> <span data-ttu-id="fbe2b-126">Um über WPD auf diese API zuzugreifen, aufrufen Sie **QueryInterface** für **IID \_ iwmdrmdeviceapp** aus dem **IStream** , der von [**iportabledevicecontent:: deateobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-126">To access this API through WPD, call **QueryInterface** on **IID\_IWMDRMDeviceApp** from the **IStream** returned from [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="fbe2b-127">Diese **iwmdrmdeviceapp** -Instanz ist an die **iportabledevice** -Verbindung mit dem WMDRM-kompatiblen Gerät gebunden, nicht an dem spezifischen Inhalt, in dem der **IStream** abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-127">This **IWMDRMDeviceApp** instance tied to the **IPortableDevice** connection to your WMDRM-compatible device, and not the specific content where the **IStream** was obtained.</span></span> <span data-ttu-id="fbe2b-128">WPD umschließt die Messungs-APIs intern und macht Sie für Ihre Anwendung zugänglich.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-128">WPD internally wraps the metering APIs and makes it accessible to your application.</span></span> <span data-ttu-id="fbe2b-129">Die Anwendung sollte die \_ \_ ptr-Konstante WPD- \_ Gerät \_ für den *iwmdmdevice* - \* Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-129">Your application should use the WMDRMDEVICEAPP\_USE\_WPD\_DEVICE\_PTR constant for the *IWMDMDevice*\* parameter.</span></span>

<span data-ttu-id="fbe2b-130">Dies wird im folgenden Code Ausschnitt veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-130">The following code snippet demonstrates this.</span></span>


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



<span data-ttu-id="fbe2b-131">Diese Voraussetzung gilt auch für den privaten Schlüssel der Anwendung und das Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-131">The same pre-requisite with the application private key and certificate applies here as well.</span></span> <span data-ttu-id="fbe2b-132">Wenn der Schlüssel/das Zertifikat ungültig ist oder das WMDRM-System nicht initialisiert werden kann, schlägt der **queryinferface** -Rückruf fehl.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-132">If the key/certificate is invalid or if the WMDRM system fails to initialize, the **QueryInferface** call will fail.</span></span>

<span data-ttu-id="fbe2b-133">Die obige Methode zum Abrufen der **iwmdrmdeviceapp** -Schnittstelle über den **IStream** -Zeiger ist nur eine einfache Möglichkeit, wenn Ihre Anwendung bereits eine zuvor geschützte Inhalts Übertragung durchführen muss, bevor Sie mit der Verarbeitung von Messungs-und Lizenz Synchronisierungs Vorgängen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-133">The above method to acquire the **IWMDRMDeviceApp** interface from the **IStream** pointer is just a convenience if your application is already doing a prior protected content transfer, before proceeding on to do metering and license synchronization operations.</span></span>

<span data-ttu-id="fbe2b-134">Die Empfehlung für die meisten Anwendungen, die auf **iwmdrmdeviceapp** zugreifen müssen, besteht darin, **iwmdrmdeviceapp** direkt zu initialisieren, da es nicht erforderlich ist, dass Ihre Anwendung geschützte Inhalte überträgt oder an den Übertragungs Schnittstellen hält, um die Geräte Messung und die Lizenz Synchronisierung durchzuführen. Diese Methode erfordert die Verwendung von WMDM-APIs (Windows Media Device Manager).</span><span class="sxs-lookup"><span data-stu-id="fbe2b-134">Our recommendation for most applications that need to access **IWMDRMDeviceApp** is to initialize **IWMDRMDeviceApp** directly as this does not require your application to transfer protected content or hold on to the transfer interfaces in order to do device metering and license sync. This method will require usage of Windows Media Device Manager (WMDM) APIs.</span></span> <span data-ttu-id="fbe2b-135">Ausführliche Informationen und Beispielcode finden Sie im Whitepaper [zugreifen auf WMDRM-APIs von einer WPD-Anwendung](../windows-portable-devices.md) auf der whdc-Website.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-135">For details and sample code, refer to the [Accessing WMDRM APIs from a WPD Application](../windows-portable-devices.md) whitepaper on the WHDC site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbe2b-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fbe2b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbe2b-137">**Tragbare Windows-Geräte**</span><span class="sxs-lookup"><span data-stu-id="fbe2b-137">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
