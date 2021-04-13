---
title: Überprüfung und Initialisierung
description: Überprüfung und Initialisierung
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- SDK für Windows Media-Format, Überprüfung
- SDK für Windows Media-Format, Initialisierung
- Digital Rights Management (DRM), Überprüfung
- DRM (Digital Rights Management), Überprüfung
- Digital Rights Management (DRM), Initialisierung
- DRM (Digital Rights Management), Initialisierung
- Erweiterte APIs für den DRM-Client, Überprüfung
- Erweiterte Client-APIs, Überprüfung
- Erweiterte APIs für den DRM-Client, Initialisierung
- Erweiterte Client-APIs, Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314309"
---
# <a name="verification-and-initialization"></a><span data-ttu-id="631ec-113">Überprüfung und Initialisierung</span><span class="sxs-lookup"><span data-stu-id="631ec-113">Verification and Initialization</span></span>

<span data-ttu-id="631ec-114">Führen Sie die folgenden Schritte aus, um zu überprüfen, ob die Transaktion zulässig ist, und um ein Objekt zu initialisieren, das den Inhalt entschlüsselt:</span><span class="sxs-lookup"><span data-stu-id="631ec-114">You should perform the following steps to verify that transcryption is allowed and to initialize an object that will decrypt the content:</span></span>

1.  <span data-ttu-id="631ec-115">Wenn Sie bereits über die Schlüssel-ID für den Inhalt verfügen, fahren Sie mit Schritt 5 fort.</span><span class="sxs-lookup"><span data-stu-id="631ec-115">If you already have the Key ID for the content, skip to step 5.</span></span>
2.  <span data-ttu-id="631ec-116">Rufen Sie die [**wmkreateeditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) -Funktion auf, um ein Metadaten-Editor-Objekt zu erstellen und eine Instanz der [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) -Schnittstelle des Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="631ec-116">Call the [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) function to create a metadata editor object and get an instance of that object's [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) interface.</span></span>
3.  <span data-ttu-id="631ec-117">Ruft **IWMMetadataEditor:: QueryInterface** auf, um eine Instanz der [**iwmdrmeditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="631ec-117">Call **IWMMetadataEditor::QueryInterface** to get an instance of the [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) interface.</span></span>
4.  <span data-ttu-id="631ec-118">Aufrufen von [**iwmdrmeditor:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) zum Abrufen der **DRM- \_ drmHeader- \_ keyid** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="631ec-118">Call [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) to get the **DRM\_DRMHeader\_KeyID** property.</span></span>
5.  <span data-ttu-id="631ec-119">Initialisieren Sie die erweiterten APIs für den Windows Media DRM-Client, indem Sie die [**wmdrmstartup**](wmdrmstartup.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="631ec-119">Initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>
6.  <span data-ttu-id="631ec-120">Rufen Sie die [**wmdrmkreateprotectedprovider**](wmdrmcreateprotectedprovider.md) -Funktion auf, um ein sicheres Anbieter Objekt zu erstellen, und rufen Sie eine Instanz der [**iwmdrmprovider**](iwmdrmprovider.md) -Schnittstelle dieses Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="631ec-120">Call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function to create a secure provider object and get an instance of that object's [**IWMDRMProvider**](iwmdrmprovider.md) interface.</span></span>
7.  <span data-ttu-id="631ec-121">Rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md) auf, um ein Lizenz Verwaltungs Objekt zu erstellen und eine Instanz seiner [**iwmdrmlicensemanagement**](iwmdrmlicensemanagement.md) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="631ec-121">Call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md) to create a license management object and get an instance of its [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span>
8.  <span data-ttu-id="631ec-122">Nennen Sie [**iwmdrmlicenaberation**](iwmdrmlicensemanagement-createlicenseenumeration.md), und übergeben Sie dabei die Schlüssel-ID und das Recht, das die Aktionen bestimmt, die mit dem Inhalt ausgeführt werden sollen, nachdem er in eine Transaktion aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="631ec-122">Call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing in the Key ID and the right that governs the actions to be taken with the content after it is transcrypted.</span></span> <span data-ttu-id="631ec-123">Dieser Befehl ruft eine Instanz der [**iwmdrmlicense**](iwmdrmlicense.md) -Schnittstelle ab, die verwendet werden kann, um alle übereinstimmenden Lizenzen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="631ec-123">This call will retrieve an instance of the [**IWMDRMLicense**](iwmdrmlicense.md) interface that can be used to enumerate through any matching licenses.</span></span>
9.  <span data-ttu-id="631ec-124">Rufen Sie [**iwmdrmlicense:: getinclusionlist**](iwmdrmlicense-getinclusionlist.md) auf, um die Liste der autorisierten Inhalts Schutzsysteme (CPS) abzurufen, die vom Lizenz Aussteller angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="631ec-124">Call [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) to retrieve the list of authorized content protection systems (CPS) as specified by the license issuer.</span></span>
10. <span data-ttu-id="631ec-125">Analysieren Sie die Aufnahme Liste, um zu bestätigen, dass die GUID der Ausgabe-CPS von der Lizenz zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="631ec-125">Parse the inclusion list to confirm that the GUID of the output CPS is allowed by the license.</span></span>
11. <span data-ttu-id="631ec-126">Wenn die gewünschte Export-GUID nicht in der Aufnahme Liste enthalten ist, nennen Sie [**iwmdrmlicense:: GetNext**](iwmdrmlicense-getnext.md) , um die nächste anwendbare Lizenz (sofern vorhanden) abzurufen, und wiederholen Sie die Schritte 9 und 10.</span><span class="sxs-lookup"><span data-stu-id="631ec-126">If the desired export GUID is not in the inclusion list, call [**IWMDRMLicense::GetNext**](iwmdrmlicense-getnext.md) to get the next applicable license (if any) and repeat steps 9 and 10.</span></span> <span data-ttu-id="631ec-127">Wenn keine Lizenz die gewünschte GUID in der Aufnahme Liste aufweist, kann der Export nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="631ec-127">If no license has the desired GUID in its inclusion list, the export cannot be performed.</span></span>
12. <span data-ttu-id="631ec-128">Rufen Sie [**iwmdrmlicense:: kreatesecuredecryptor**](iwmdrmlicense-createsecuredecryptor.md) auf, um ein Entschlüsselungs-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="631ec-128">Call [**IWMDRMLicense::CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) to create a decryptor object.</span></span> <span data-ttu-id="631ec-129">Übergeben Sie das Anwendungs Zertifikat exportieren.</span><span class="sxs-lookup"><span data-stu-id="631ec-129">Pass in the export application certificate.</span></span> <span data-ttu-id="631ec-130">Dieser Befehl stellt einen Zeiger auf eine Instanz der [**iwmdrmentschlüsselungsschnittstelle**](iwmdrmdecrypt.md) des Entschlüsselungs-Objekts und ein binäres Objekt bereit, das den Ausgangswert enthält.</span><span class="sxs-lookup"><span data-stu-id="631ec-130">This call will provide a pointer to an instance of the decryptor object's [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface and a binary object containing the seed.</span></span> <span data-ttu-id="631ec-131">Zurzeit wird nur die Windows Media **DRM- \_ \_ Schutztyp \_ RC4** -Konstante als Argument für den *dwFlags* -Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="631ec-131">Only the Windows Media **DRM\_PROTECTION\_TYPE\_RC4** constant is supported as an argument to the *dwFlags* parameter at this time.</span></span>
13. <span data-ttu-id="631ec-132">Verwenden Sie das RSA OAEP-Verschlüsselungsschema, um den Initialisierungs Vektor zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="631ec-132">Use the RSA OAEP encryption scheme to decrypt the initialization vector.</span></span>
14. <span data-ttu-id="631ec-133">Verwenden Sie die von Microsoft bereitgestellte ASF-Bibliotheks Bibliothek, wenn Sie in den Windows Media DRM-Exportvertrag eintreten, um den Offset für jede Nutzlast in Bytes zu finden.</span><span class="sxs-lookup"><span data-stu-id="631ec-133">Use the ASF parsing library provided by Microsoft when you enter into the Windows Media DRM export agreement, to locate the offset in bytes for each payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="631ec-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="631ec-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="631ec-135">**Exportieren von komprimiertem Inhalt**</span><span class="sxs-lookup"><span data-stu-id="631ec-135">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




