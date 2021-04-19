---
description: Wird verwendet, um eine Verbindung mit einem Netzwerk herzustellen, das Protected Extensible Authentication Protocol mit dem Microsoft Challenge Handshake Authentication Protocol Version 2 (Peer-MSCHAPv2) mit Benutzername/Kennwort für 802.1 x-Authentifizierung verwendet.
ms.assetid: b5dde0d0-940f-40ec-b24d-95a76325ff1b
title: Beispiel für ein Peer-Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db34a3a99305f3506e3b34fde48f41e5a4c72ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348594"
---
# <a name="peap-profile-sample"></a><span data-ttu-id="2b746-103">Beispiel für ein Peer-Profil</span><span class="sxs-lookup"><span data-stu-id="2b746-103">PEAP Profile Sample</span></span>

<span data-ttu-id="2b746-104">Dieses Profil Beispiel zeigt ein Kabelnetzwerk Profil, das zum Herstellen einer Verbindung mit einem Netzwerk verwendet wird, das Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol Version 2 (Peer-MSCHAPv2) mit \* username \* **/** _Password_ für 802.1 x-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b746-104">This profile sample shows a wired network profile used to connect to a network that uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ for 802.1X authentication.</span></span> <span data-ttu-id="2b746-105">Der Benutzer wird aufgefordert, Anmelde Informationen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="2b746-105">The user is prompted to enter credentials.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<LANProfile xmlns="https://www.microsoft.com/networking/LAN/profile/v1">
    <MSM>
        <security>
            <OneXEnforced>false</OneXEnforced>
            <OneXEnabled>true</OneXEnabled>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
                        <EapMethod>
                            <eapCommon:Type>25</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                       </EapMethod>
                       <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                               xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
                               xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
                           <baseEap:Eap>
                               <baseEap:Type>25</baseEap:Type> 
                               <msPeap:EapType>
                                   <msPeap:ServerValidation>
                                       <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
                                       <msPeap:TrustedRootCA /> 
                                   </msPeap:ServerValidation>
                                   <msPeap:FastReconnect>true</msPeap:FastReconnect> 
                                   <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
                                   <baseEap:Eap>
                                       <baseEap:Type>26</baseEap:Type> 
                                       <msChapV2:EapType>
                                           <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
                                       </msChapV2:EapType>
                                   </baseEap:Eap>
                                   <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
                                   <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
                                   <msPeap:PeapExtensions /> 
                               </msPeap:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</LANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="2b746-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b746-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b746-107">Beispiele für kabelgebundene profile</span><span class="sxs-lookup"><span data-stu-id="2b746-107">Wired Profile Samples</span></span>](wired-profile-samples.md)
</dt> </dl>

 

 



