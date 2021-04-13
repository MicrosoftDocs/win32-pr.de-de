---
title: Die Methode "kreateselfsignedcertificate" der Win32_TSGatewayServer-Klasse
description: Erstellt ein selbst signiertes Zertifikat und gibt den Zertifikat Hash als \ 0034; out \ 0034; zurück. Parame.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "kreateselfsignedcertificate"
- Methode Remotedesktopdienste der Methode "kreateselfsignedcertificate", Win32_TSGatewayServer Klasse
- Win32_TSGatewayServer-Klasse Remotedesktopdienste, Methode "kreateselfsignedcertificate"
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475639"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="67a0c-106">Methode "| ateselfsignedcertificate" der Win32-Klasse "t- \_ Gatewayserver"</span><span class="sxs-lookup"><span data-stu-id="67a0c-106">CreateSelfSignedCertificate method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="67a0c-107">Erstellt ein selbst signiertes Zertifikat und gibt den Zertifikat Hash als einen out-Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="67a0c-107">Creates a self-signed certificate and returns the certificate hash as an "out" parameter.</span></span> <span data-ttu-id="67a0c-108">Außerdem wird der Text "TS- \_ Gateway \_ selbst \_ signiertes \_ Zertifikat" der Zertifikat Kontext Eigenschaft hinzugefügt, sodass das Zertifikat als Remotedesktop Gateway-Zertifikat (RD-Gateway) erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="67a0c-108">Also, adds the text "TS\_GATEWAY\_SELF\_SIGNED\_CERTIFICATE" to the certificate context property so that the certificate is recognized as a Remote Desktop Gateway (RD Gateway) certificate.</span></span> <span data-ttu-id="67a0c-109">Diese Methode verwendet einen RD-Gateway spezifischen Schlüssel Container, um das Zertifikat zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67a0c-109">This method uses an RD Gateway-specific key container to create the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a0c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="67a0c-110">Syntax</span></span>


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="67a0c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="67a0c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a0c-112">*Subjetname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67a0c-112">*SubjectName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67a0c-113">Der Antragsteller Name des selbst signierten Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="67a0c-113">Subject name of the self-signed certificate.</span></span>

</dd> <dt>

<span data-ttu-id="67a0c-114">*CertHash* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="67a0c-114">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67a0c-115">Der Zertifikat Hash.</span><span class="sxs-lookup"><span data-stu-id="67a0c-115">The certificate hash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67a0c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67a0c-116">Remarks</span></span>

<span data-ttu-id="67a0c-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="67a0c-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="67a0c-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="67a0c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="67a0c-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="67a0c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="67a0c-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67a0c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="67a0c-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="67a0c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="67a0c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67a0c-122">Requirements</span></span>



| <span data-ttu-id="67a0c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67a0c-123">Requirement</span></span> | <span data-ttu-id="67a0c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="67a0c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a0c-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67a0c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="67a0c-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="67a0c-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="67a0c-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67a0c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="67a0c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67a0c-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="67a0c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="67a0c-129">Namespace</span></span><br/>                | <span data-ttu-id="67a0c-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="67a0c-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="67a0c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="67a0c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67a0c-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="67a0c-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="67a0c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="67a0c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67a0c-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67a0c-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="67a0c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67a0c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a0c-136">**Win32- \_ Gatewayserver**</span><span class="sxs-lookup"><span data-stu-id="67a0c-136">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

