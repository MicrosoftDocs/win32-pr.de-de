---
description: Gibt 802.1 x-Konfigurationsinformationen für ein Kabel-oder Drahtlos LAN-Profil an.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: Onex-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363447"
---
# <a name="onex-element"></a><span data-ttu-id="adb8a-103">Onex-Element</span><span class="sxs-lookup"><span data-stu-id="adb8a-103">OneX Element</span></span>

<span data-ttu-id="adb8a-104">Das Onex-Element gibt 802.1 x-Konfigurationsinformationen für ein Kabel-oder Drahtlos LAN-Profil an.</span><span class="sxs-lookup"><span data-stu-id="adb8a-104">The OneX element specifies 802.1X configuration information for a wired or wireless LAN profile.</span></span> <span data-ttu-id="adb8a-105">Dieses Element ist das eindeutige root-Element für ein 802.1 x-Profil.</span><span class="sxs-lookup"><span data-stu-id="adb8a-105">This element is the unique root element for an 802.1X profile.</span></span>

<span data-ttu-id="adb8a-106">Der Ziel Namespace für das Onex-Element ist `https://www.microsoft.com/networking/OneX/v1` .</span><span class="sxs-lookup"><span data-stu-id="adb8a-106">The target namespace for the OneX element is `https://www.microsoft.com/networking/OneX/v1`.</span></span> <span data-ttu-id="adb8a-107">Die meisten untergeordneten Elemente des Onex-Elements befinden sich im- `OneX` Namespace.</span><span class="sxs-lookup"><span data-stu-id="adb8a-107">Most child elements of the OneX element are in the `OneX` namespace.</span></span> <span data-ttu-id="adb8a-108">Es gibt eine Ausnahme: das [**eapconfig**](onexschema-eapconfig-onex-element.md) -Element befindet sich im- `https://www.microsoft.com/provisioning/EapHostConfig` Namespace.</span><span class="sxs-lookup"><span data-stu-id="adb8a-108">There is one exception: the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span>

<span data-ttu-id="adb8a-109">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Nur das [**eapconfig**](onexschema-eapconfig-onex-element.md) -Element wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="adb8a-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported.</span></span> <span data-ttu-id="adb8a-110">Andere Elemente, sofern Sie in einem Profil vorhanden sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="adb8a-110">Other elements, if present in a profile, will be ignored.</span></span>

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="type"
                            minOccurs="1"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="preLogon"
                                     />
                                    <xs:enumeration
                                        value="postLogon"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="maxDelay"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:enumeration
                                        value="0"
                                     />
                                    <xs:enumeration
                                        value="120"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="userBasedVirtualLan"
                            type="boolean"
                            minOccurs="0"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="adb8a-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="adb8a-111">Child elements</span></span>



| <span data-ttu-id="adb8a-112">Element</span><span class="sxs-lookup"><span data-stu-id="adb8a-112">Element</span></span>                                                                            | <span data-ttu-id="adb8a-113">type</span><span class="sxs-lookup"><span data-stu-id="adb8a-113">Type</span></span>    | <span data-ttu-id="adb8a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adb8a-114">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="adb8a-115">**authmode**</span><span class="sxs-lookup"><span data-stu-id="adb8a-115">**authMode**</span></span>](onexschema-authmode-onex-element.md)                               |         | <span data-ttu-id="adb8a-116">Gibt den Typ der für die Authentifizierung verwendeten Anmelde Informationen an.</span><span class="sxs-lookup"><span data-stu-id="adb8a-116">Specifies the type of credentials used for authentication.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="adb8a-117">**authperiod**</span><span class="sxs-lookup"><span data-stu-id="adb8a-117">**authPeriod**</span></span>](onexschema-authperiod-onex-element.md)                           |         | <span data-ttu-id="adb8a-118">Gibt die maximale Zeitspanne in Sekunden an, in der ein Client auf eine Antwort vom Authentifikator wartet.</span><span class="sxs-lookup"><span data-stu-id="adb8a-118">Specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="adb8a-119">**cacheuserdata**</span><span class="sxs-lookup"><span data-stu-id="adb8a-119">**cacheUserData**</span></span>](onexschema-cacheuserdata-onex-element.md)                     | <span data-ttu-id="adb8a-120">boolean</span><span class="sxs-lookup"><span data-stu-id="adb8a-120">boolean</span></span> | <span data-ttu-id="adb8a-121">Gibt an, ob die Benutzer Anmelde Informationen für nachfolgende Verbindungen zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="adb8a-121">Specifies whether the user credentials are cached for subsequent connections.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="adb8a-122">**Eapconfig**</span><span class="sxs-lookup"><span data-stu-id="adb8a-122">**EAPConfig**</span></span>](onexschema-eapconfig-onex-element.md)                             |         | <span data-ttu-id="adb8a-123">Gibt die EAPHost-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="adb8a-123">Specifies the EAPHost configuration.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="adb8a-124">**heldperiod**</span><span class="sxs-lookup"><span data-stu-id="adb8a-124">**heldPeriod**</span></span>](onexschema-heldperiod-onex-element.md)                           |         | <span data-ttu-id="adb8a-125">Gibt die Zeitdauer in Sekunden an, in der ein Client die Authentifizierung nach einem fehlgeschlagenen Authentifizierungs Versuch nicht erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="adb8a-125">Specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span><br/>                                                                             |
| [<span data-ttu-id="adb8a-126">**maxauthfailure**</span><span class="sxs-lookup"><span data-stu-id="adb8a-126">**maxAuthFailures**</span></span>](onexschema-maxauthfailures-onex-element.md)                 |         | <span data-ttu-id="adb8a-127">Gibt die maximale Anzahl von Authentifizierungs Fehlern an, die für einen Satz von Anmelde Informationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="adb8a-127">Specifies the maximum number of authentication failures allowed for a set of credentials.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="adb8a-128">**MaxDelay**</span><span class="sxs-lookup"><span data-stu-id="adb8a-128">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="adb8a-129">Gibt die maximale Verzögerung in Sekunden an, bevor der Single Sign-on Verbindungsversuch fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="adb8a-129">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="adb8a-130">**maxstart**</span><span class="sxs-lookup"><span data-stu-id="adb8a-130">**maxStart**</span></span>](onexschema-maxstart-onex-element.md)                               |         | <span data-ttu-id="adb8a-131">Gibt die maximale Anzahl von EAPOL-Start gesendeten Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="adb8a-131">Specifies the maximum number of EAPOL-Start messages sent.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="adb8a-132">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="adb8a-132">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)                       |         | <span data-ttu-id="adb8a-133">Gibt Single Sign-on Netzwerk-Konfigurationsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="adb8a-133">Specifies single sign-on network configuration information.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="adb8a-134">**startperiod**</span><span class="sxs-lookup"><span data-stu-id="adb8a-134">**startPeriod**</span></span>](onexschema-startperiod-onex-element.md)                         |         | <span data-ttu-id="adb8a-135">Gibt die Zeitdauer in Sekunden an, die gewartet werden soll, bevor eine EAPOL-Start gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="adb8a-135">Specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="adb8a-136">**supplicantmode**</span><span class="sxs-lookup"><span data-stu-id="adb8a-136">**supplicantMode**</span></span>](onexschema-supplicantmode-onex-element.md)                   |         | <span data-ttu-id="adb8a-137">Gibt die für EAPOL-Pakete verwendete Übertragungsmethode an.</span><span class="sxs-lookup"><span data-stu-id="adb8a-137">Specifies the method of transmission used for EAPOL packets.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="adb8a-138">**Sorte**</span><span class="sxs-lookup"><span data-stu-id="adb8a-138">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="adb8a-139">Gibt an, wann Single Sign-on ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="adb8a-139">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="adb8a-140">Wenn diese Einstellung auf festgelegt `preLogon` ist, wird Single Sign-on ausgeführt, bevor sich der Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="adb8a-140">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="adb8a-141">Wenn diese Einstellung auf festgelegt `postLogon` ist, wird Single Sign-on sofort nach der Anmeldung des Benutzers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="adb8a-141">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="adb8a-142">**userbasedvirtuallan**</span><span class="sxs-lookup"><span data-stu-id="adb8a-142">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="adb8a-143">boolean</span><span class="sxs-lookup"><span data-stu-id="adb8a-143">boolean</span></span> | <span data-ttu-id="adb8a-144">Gibt an, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird.</span><span class="sxs-lookup"><span data-stu-id="adb8a-144">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="adb8a-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adb8a-145">Remarks</span></span>

<span data-ttu-id="adb8a-146">Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer Struktur ähnlichen Struktur finden Sie unter [Onex-Schema Elemente](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="adb8a-146">To view the list of child elements in a tree-like structure, see [OneX Schema Elements](onexschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="adb8a-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adb8a-147">Requirements</span></span>



| <span data-ttu-id="adb8a-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adb8a-148">Requirement</span></span> | <span data-ttu-id="adb8a-149">Wert</span><span class="sxs-lookup"><span data-stu-id="adb8a-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="adb8a-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adb8a-150">Minimum supported client</span></span><br/> | <span data-ttu-id="adb8a-151">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adb8a-151">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="adb8a-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adb8a-152">Minimum supported server</span></span><br/> | <span data-ttu-id="adb8a-153">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adb8a-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="adb8a-154">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="adb8a-154">Redistributable</span></span><br/>          | <span data-ttu-id="adb8a-155">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="adb8a-155">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




