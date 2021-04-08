---
title: Win32_TSGeneralSetting-Klasse
description: Stellt allgemeine Einstellungen des Terminals dar, z. b. die Verschlüsselungs Stufe und das Transportprotokoll.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting-Klasse Remotedesktopdienste
- Win32_TSGeneralSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741776"
---
# <a name="win32_tsgeneralsetting-class"></a><span data-ttu-id="8122b-105">Win32-Klasse "t \_ General setting"</span><span class="sxs-lookup"><span data-stu-id="8122b-105">Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="8122b-106">Die **Win32 \_ tgeneralsetting** -WMI-Klasse stellt allgemeine Einstellungen des Terminals dar, z. b. die Verschlüsselungs Stufe und das Transportprotokoll.</span><span class="sxs-lookup"><span data-stu-id="8122b-106">The **Win32\_TSGeneralSetting** WMI class represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

<span data-ttu-id="8122b-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="8122b-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="8122b-108">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8122b-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="8122b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8122b-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="8122b-110">Member</span><span class="sxs-lookup"><span data-stu-id="8122b-110">Members</span></span>

<span data-ttu-id="8122b-111">Die Win32-Klasse " **\_ zgeneralsetting** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8122b-111">The **Win32\_TSGeneralSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8122b-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="8122b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8122b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8122b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8122b-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="8122b-114">Methods</span></span>

<span data-ttu-id="8122b-115">Die Win32-Klasse " **\_ zgeneralsetting** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8122b-115">The **Win32\_TSGeneralSetting** class has these methods.</span></span>



| <span data-ttu-id="8122b-116">Methode</span><span class="sxs-lookup"><span data-stu-id="8122b-116">Method</span></span>                                                                                        | <span data-ttu-id="8122b-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8122b-117">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8122b-118">**Setencryptionlevel**</span><span class="sxs-lookup"><span data-stu-id="8122b-118">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)                       | <span data-ttu-id="8122b-119">Legt die Verschlüsselungs Stufe fest.</span><span class="sxs-lookup"><span data-stu-id="8122b-119">Sets the encryption level.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="8122b-120">**Setsecuritylayer**</span><span class="sxs-lookup"><span data-stu-id="8122b-120">**SetSecurityLayer**</span></span>](win32-tsgeneralsetting-setsecuritylayer.md)                           | <span data-ttu-id="8122b-121">Legt die Sicherheitsstufe auf "RDP Security Layer" (0), "aushandeln" (1) oder "SSL" (2) fest.</span><span class="sxs-lookup"><span data-stu-id="8122b-121">Sets the security layer to one of "RDP Security Layer" (0), "Negotiate" (1), or "SSL" (2).</span></span><br/>                                                                   |
| [<span data-ttu-id="8122b-122">**Setuserauthenticationrequired**</span><span class="sxs-lookup"><span data-stu-id="8122b-122">**SetUserAuthenticationRequired**</span></span>](setuserauthenticationrequired-win32-tsgeneralsetting.md) | <span data-ttu-id="8122b-123">Aktiviert oder deaktiviert die Anforderung, dass Benutzer zur Verbindungszeit authentifiziert werden müssen, indem der Wert der **UserAuthenticationRequired** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8122b-123">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8122b-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8122b-124">Properties</span></span>

<span data-ttu-id="8122b-125">Die Win32-Klasse "t- **\_ generalsetting** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8122b-125">The **Win32\_TSGeneralSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8122b-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8122b-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8122b-129">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8122b-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8122b-130">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8122b-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8122b-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8122b-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8122b-132">**CertificateName**</span><span class="sxs-lookup"><span data-stu-id="8122b-132">**CertificateName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-135">Anzeige Name für den Antragsteller Namen des persönlichen Zertifikats für den lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="8122b-135">Display name for the local computer personal certificate subject name.</span></span>

</dd> <dt>

<span data-ttu-id="8122b-136">**Zertifikate**</span><span class="sxs-lookup"><span data-stu-id="8122b-136">**Certificates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-137">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="8122b-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8122b-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-139">Enthält einen serialisierten Zertifikat Speicher, der alle Zertifikate aus dem **eigenen Benutzerkonten** Speicher auf dem Computer enthält, bei denen es sich um gültige Server Zertifikate für die Verwendung mit SSL (Secure Sockets Layer) handelt.</span><span class="sxs-lookup"><span data-stu-id="8122b-139">Contains a serialized certificate store that contains all of the certificates from the **My user account** store on the computer that are valid server certificates for use with secure sockets layer (SSL).</span></span>

</dd> <dt>

<span data-ttu-id="8122b-140">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="8122b-140">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8122b-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8122b-143">Beschreibender Name der Kombination aus Sitzungsschicht und Transportprotokoll.</span><span class="sxs-lookup"><span data-stu-id="8122b-143">Descriptive name of the combination of session layer and transport protocol.</span></span>

</dd> <dt>

<span data-ttu-id="8122b-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8122b-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-147">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8122b-147">Description of the object.</span></span>

<span data-ttu-id="8122b-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8122b-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8122b-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8122b-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-150">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8122b-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8122b-152">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="8122b-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8122b-153">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8122b-153">The date the object was installed.</span></span> <span data-ttu-id="8122b-154">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8122b-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8122b-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8122b-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8122b-156">**Minverschlüsselungslevel**</span><span class="sxs-lookup"><span data-stu-id="8122b-156">**MinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8122b-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8122b-159">Qualifizierer: **niedrig** ("nur Daten, die vom Client an den Server gesendet werden, werden durch Verschlüsselung basierend auf der Standardschlüssel Stärke des Servers geschützt.</span><span class="sxs-lookup"><span data-stu-id="8122b-159">Qualifiers: **Low** ("Only data sent from client to server is protected by encryption based on server's standard key strength.</span></span> <span data-ttu-id="8122b-160">Die vom Server an den Client gesendeten Daten sind nicht geschützt. "), **Mittel** (" alle Daten, die zwischen dem Server und dem Client gesendet werden, werden durch Verschlüsselung basierend auf der Standardschlüssel Stärke des Servers geschützt. "), **hoch** (" alle Daten, die zwischen Server und Client gesendet werden, werden durch die Verschlüsselungs basierte maximale Schlüssel Stärke von onServer geschützt. ")</span><span class="sxs-lookup"><span data-stu-id="8122b-160">Data sent from Server to client is not protected."), **Medium** ("All data sent between Server and client is protected by encryption based on server's standard key strength."), **High** ("All data sent between Server and client is protected by encryption based onserver's maximum key strength.")</span></span>
</dt> </dl>

<span data-ttu-id="8122b-161">Die minimale Verschlüsselungs Stufe.</span><span class="sxs-lookup"><span data-stu-id="8122b-161">The minimum encryption level.</span></span>

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="8122b-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (1)</span><span class="sxs-lookup"><span data-stu-id="8122b-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-163">Niedriger Verschlüsselungs Grad.</span><span class="sxs-lookup"><span data-stu-id="8122b-163">Low level of encryption.</span></span> <span data-ttu-id="8122b-164">Nur vom Client an den Server gesendete Daten werden mithilfe der 56-Bit-Verschlüsselung verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8122b-164">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="8122b-165">Beachten Sie, dass die vom Server an den Client gesendeten Daten nicht verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="8122b-165">Be aware that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span data-ttu-id="8122b-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Mittel/Client kompatibel** (2)</span><span class="sxs-lookup"><span data-stu-id="8122b-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Medium / Client Compatible** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-167">Client kompatibler Verschlüsselungs Grad.</span><span class="sxs-lookup"><span data-stu-id="8122b-167">Client compatible level of encryption.</span></span> <span data-ttu-id="8122b-168">Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden mit der maximalen Schlüssel Stärke verschlüsselt, die vom Client unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8122b-168">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="8122b-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (3)</span><span class="sxs-lookup"><span data-stu-id="8122b-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-170">Hohes Maß an Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="8122b-170">High level of encryption.</span></span> <span data-ttu-id="8122b-171">Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden mit starker 128-Bit-Verschlüsselung verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8122b-171">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="8122b-172">Clients, die diese Verschlüsselungs Stufe nicht unterstützen, können keine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="8122b-172">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span data-ttu-id="8122b-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Kompatibel** mit der Konformität (4)</span><span class="sxs-lookup"><span data-stu-id="8122b-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**FIPS Compliant** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-174">Mit Aktivier barer Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="8122b-174">FIPS compliant encryption.</span></span> <span data-ttu-id="8122b-175">Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden verschlüsselt und mit den Federal Information Processing Standard (FI)-Verschlüsselungsalgorithmen mithilfe der Kryptografiemodule von Microsoft entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8122b-175">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="8122b-176">Der Standardwert für "Sicherheitsanforderungen für kryptografische Module" ist "Standard".</span><span class="sxs-lookup"><span data-stu-id="8122b-176">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="8122b-177">In den Informationen zu den in der US-Regierung verwendeten Hardware-und Softwaremodulen werden die behördlichen Anforderungen für Hardware-und Software Kryptografiemodule beschrieben. 2001 140-2 1994 140-1</span><span class="sxs-lookup"><span data-stu-id="8122b-177">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8122b-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="8122b-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-181">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8122b-181">The name of the object.</span></span>

<span data-ttu-id="8122b-182">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8122b-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8122b-183">**Policysourceminverschlüsselunglevel**</span><span class="sxs-lookup"><span data-stu-id="8122b-183">**PolicySourceMinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-184">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8122b-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-186">Gibt an, ob die **minverschlüsseltionlevel** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="8122b-186">Indicates whether the **MinEncryptionLevel** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8122b-187">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8122b-187">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-188">Server</span><span class="sxs-lookup"><span data-stu-id="8122b-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="8122b-189">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8122b-189">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-190">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8122b-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8122b-191">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="8122b-191">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-192">Standard</span><span class="sxs-lookup"><span data-stu-id="8122b-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8122b-193">**Policysourcesecuritylayer**</span><span class="sxs-lookup"><span data-stu-id="8122b-193">**PolicySourceSecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-194">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8122b-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-196">Gibt an, ob die **securitylayer** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="8122b-196">Indicates whether the **SecurityLayer** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8122b-197">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8122b-197">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-198">Server</span><span class="sxs-lookup"><span data-stu-id="8122b-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="8122b-199">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8122b-199">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-200">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8122b-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8122b-201">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="8122b-201">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-202">Standard</span><span class="sxs-lookup"><span data-stu-id="8122b-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8122b-203">**Policysourceuserauthenticationrequired**</span><span class="sxs-lookup"><span data-stu-id="8122b-203">**PolicySourceUserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-204">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8122b-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-206">Gibt an, ob die **UserAuthenticationRequired** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="8122b-206">Indicates whether the **UserAuthenticationRequired** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8122b-207">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8122b-207">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-208">Server</span><span class="sxs-lookup"><span data-stu-id="8122b-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="8122b-209">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8122b-209">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-210">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8122b-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8122b-211">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="8122b-211">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-212">Standard</span><span class="sxs-lookup"><span data-stu-id="8122b-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8122b-213">**SecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="8122b-213">**SecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-214">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8122b-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8122b-216">Qualifizierer: **rdpsecuritylayer** ("RDP-Sicherheitsebene: Kommunikation zwischen dem Server und der Client verwendet die Native RDP-Verschlüsselung"), **Aushandlungs** ("die sicherste Ebene, die vom Client unterstützt wird, wird verwendet. Wenn unterstützt, wird TLS 1,0 verwendet. "), **SSL** (" SSL (TLS 1,0) "wird für die Server Authentifizierung verwendet, und alle Daten, die zwischen dem Server und dem Client übertragen werden, werden verschlüsselt. Diese Einstellung erfordert, dass der Server über ein SSL-kompatibles Zertifikat verfügt. "), **newtbd** (" eine neue Sicherheitsebene in Longhorn ")</span><span class="sxs-lookup"><span data-stu-id="8122b-216">Qualifiers: **RDPSecurityLayer** ("RDP Security Layer: Communication between the serverand the client will use native RDP encryption."), **Negotiate** ("The most secure layer that is supported by the client will be used.If supported, TLS 1.0 will be used."), **SSL** ("SSL (TLS 1.0) will be used for server authentication as well as forencrypting all data transferred between the server and the client.This setting requires the server to have an SSL compatible certificate."), **NEWTBD** ("A NEW SECURITY LAYER in LONGHORN.")</span></span>
</dt> </dl>

<span data-ttu-id="8122b-217">Gibt die Sicherheitsebene an, die zwischen dem Client und dem Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8122b-217">Specifies the security layer used between the client and server.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="8122b-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP-Sicherheitsebene** (1)</span><span class="sxs-lookup"><span data-stu-id="8122b-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-219">Bei der Kommunikation zwischen dem Server und dem Client wird die Native RDP-Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8122b-219">Communication between the server and the client uses native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="8122b-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Aushandeln** (2)</span><span class="sxs-lookup"><span data-stu-id="8122b-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-221">Die sicherste Ebene, die vom Client unterstützt wird, wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="8122b-221">The most secure layer that is supported by the client is used.</span></span> <span data-ttu-id="8122b-222">Wenn unterstützt, wird SSL (TLS 1,0) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8122b-222">If supported, SSL (TLS 1.0) is used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="8122b-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span><span class="sxs-lookup"><span data-stu-id="8122b-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-224">SSL (TLS 1,0) wird für die Server Authentifizierung und für die Verschlüsselung aller Daten verwendet, die zwischen dem Server und dem Client übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="8122b-224">SSL (TLS 1.0) is used for server authentication and for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="8122b-225">Diese Einstellung erfordert, dass der Server über ein SSL-kompatibles Zertifikat verfügt.</span><span class="sxs-lookup"><span data-stu-id="8122b-225">This setting requires the server to have an SSL-compatible certificate.</span></span> <span data-ttu-id="8122b-226">Diese Einstellung ist nicht kompatibel mit dem **minverschlüsseltionlevel** -Wert 1.</span><span class="sxs-lookup"><span data-stu-id="8122b-226">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span data-ttu-id="8122b-227"><span id="NEWTBD"></span><span id="newtbd"></span>**Newtbd** (4)</span><span class="sxs-lookup"><span data-stu-id="8122b-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-228">Eine neue Sicherheitsebene.</span><span class="sxs-lookup"><span data-stu-id="8122b-228">A new security layer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8122b-229">**SSLCertificateSHA1Hash**</span><span class="sxs-lookup"><span data-stu-id="8122b-229">**SSLCertificateSHA1Hash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-231">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8122b-231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8122b-232">Gibt den SHA1-Hash im Hexadezimal Format des SSL-Zertifikats an, das vom Zielserver verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8122b-232">Specifies the SHA1 hash in hexadecimal format of the SSL certificate for the target server to use.</span></span>

<span data-ttu-id="8122b-233">Sie finden den Fingerabdruck eines Zertifikats mithilfe des MMC-Snap-Ins "Zertifikate" auf der Registerkarte "Details" auf der Seite "Zertifikat Eigenschaften".</span><span class="sxs-lookup"><span data-stu-id="8122b-233">The thumbprint of a certificate may be found using the Certificates MMC snap-in on the Details tab of the certificate properties page.</span></span>

</dd> <dt>

<span data-ttu-id="8122b-234">**SSLCertificateSHA1HashType**</span><span class="sxs-lookup"><span data-stu-id="8122b-234">**SSLCertificateSHA1HashType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-235">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8122b-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-237">Gibt den Status der **SSLCertificateSHA1Hash** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="8122b-237">Indicates the state of the **SSLCertificateSHA1Hash** property.</span></span>

<dt>

<span data-ttu-id="8122b-238">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8122b-238">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-239">Ungültig</span><span class="sxs-lookup"><span data-stu-id="8122b-239">Not valid</span></span>

</dd> <dt>

<span data-ttu-id="8122b-240">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8122b-240">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-241">Standardmäßig selbst signiert</span><span class="sxs-lookup"><span data-stu-id="8122b-241">Default self-signed</span></span>

</dd> <dt>

<span data-ttu-id="8122b-242">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="8122b-242">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-243">Standard Gruppenrichtlinie erzwungen</span><span class="sxs-lookup"><span data-stu-id="8122b-243">Default group policy enforced</span></span>

</dd> <dt>

<span data-ttu-id="8122b-244">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="8122b-244">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="8122b-245">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="8122b-245">Custom</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8122b-246">**Status**</span><span class="sxs-lookup"><span data-stu-id="8122b-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8122b-249">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8122b-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8122b-250">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8122b-250">Current status of the object.</span></span> <span data-ttu-id="8122b-251">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8122b-251">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8122b-252">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="8122b-252">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8122b-253">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="8122b-253">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8122b-254">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8122b-254">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8122b-255">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="8122b-255">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8122b-256">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8122b-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8122b-257">("OK")</span><span class="sxs-lookup"><span data-stu-id="8122b-257">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8122b-258">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8122b-258">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8122b-259">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8122b-259">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8122b-260">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8122b-260">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8122b-261">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8122b-261">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8122b-262">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8122b-262">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8122b-263">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="8122b-263">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8122b-264">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8122b-264">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8122b-265">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="8122b-265">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-266">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-268">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="8122b-268">The name of the terminal.</span></span>

<span data-ttu-id="8122b-269">Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8122b-269">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8122b-270">**TerminalProtocol**</span><span class="sxs-lookup"><span data-stu-id="8122b-270">**TerminalProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-271">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-273">Der Name des Sitzungsschicht Protokolls. Beispiel: Microsoft RDP 5,0.</span><span class="sxs-lookup"><span data-stu-id="8122b-273">The name of the session layer protocol; for example, Microsoft RDP 5.0.</span></span>

</dd> <dt>

<span data-ttu-id="8122b-274">**Transport**</span><span class="sxs-lookup"><span data-stu-id="8122b-274">**Transport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-275">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8122b-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-277">Der Transporttyp, der in der Verbindung verwendet wird. beispielsweise TCP, NetBIOS oder IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="8122b-277">The type of transport used in the connection; for example, TCP, NetBIOS, or IPX/SPX.</span></span>

</dd> <dt>

<span data-ttu-id="8122b-278">**UserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="8122b-278">**UserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-279">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8122b-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8122b-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8122b-281">Gibt den Typ der Benutzerauthentifizierung an, die für Remote Verbindungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8122b-281">Specifies the type of user authentication used for remote connections.</span></span> <span data-ttu-id="8122b-282">Wenn der Wert auf 1 festgelegt ist, bedeutet dies, dass **UserAuthenticationRequired** zur Verbindungszeit eine Benutzerauthentifizierung erfordert, um den Server Schutz vor Netzwerk Angriffen zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8122b-282">If set to 1, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="8122b-283">Nur [Remotedesktopprotokoll](remote-desktop-protocol.md) (RDP)-Clients, die RDP-Version 6,0 oder höher unterstützen, können eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="8122b-283">Only [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="8122b-284">Um Unterbrechungen für Remote Benutzer zu vermeiden, wird empfohlen, RDP-Clients bereitzustellen, die die entsprechende Protokollversion unterstützen, bevor Sie die-Eigenschaft aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8122b-284">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

<span data-ttu-id="8122b-285">Verwenden Sie die [**setuserauthenticationrequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) -Methode, um diese Eigenschaft zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8122b-285">Use the [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) method to enable or disable this property.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8122b-286"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8122b-286"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-287">Die Benutzerauthentifizierung bei Verbindung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8122b-287">User authentication at connection is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8122b-288"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8122b-288"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-289">Die Benutzerauthentifizierung bei Verbindung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8122b-289">User authentication at connection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8122b-290">**WindowsAuthentication**</span><span class="sxs-lookup"><span data-stu-id="8122b-290">**WindowsAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8122b-291">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8122b-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8122b-292">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8122b-292">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8122b-293">Gibt an, ob die Verbindung standardmäßig auf den standardmäßigen Windows-Authentifizierungsprozess oder auf ein anderes auf dem System installiertes Authentifizierungs Paket festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8122b-293">Specifies whether the connection defaults to the standard Windows authentication process or to another authentication package that has been installed on the system.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8122b-294"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8122b-294"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-295">Der standardmäßige Windows-Authentifizierungsprozess wird nicht standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="8122b-295">Does not default to the standard Windows authentication process.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8122b-296"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8122b-296"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8122b-297">Standardmäßig wird der Windows-Authentifizierungsprozess standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="8122b-297">Defaults to the standard Windows authentication process.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8122b-298">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8122b-298">Remarks</span></span>

<span data-ttu-id="8122b-299">Beachten Sie, dass Windows-Stationen, die nicht der Konsolen Sitzung zugeordnet sind, nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="8122b-299">Be aware that window stations not associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="8122b-300">Wenn ein Versuch unternommen wird, indem "Console" als Wert der Terminalname-Eigenschaft angegeben wird, wird **WBEM \_ E \_ \_** von Methoden dieses Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8122b-300">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="8122b-301">Dieser Fehlercode wird auch zurückgegeben, wenn eine Fenster Station versucht, Methoden dieses Objekts zum Hinzufügen oder Ändern der Sicherheitseigenschaften der Konten "LocalSystem", "LocalService" oder "Network Service" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="8122b-301">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="8122b-302">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="8122b-302">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="8122b-303">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="8122b-303">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="8122b-304">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="8122b-304">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="8122b-305">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8122b-305">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="8122b-306">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8122b-306">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8122b-307">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="8122b-307">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8122b-308">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8122b-308">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8122b-309">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8122b-309">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8122b-310">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8122b-310">Requirements</span></span>



| <span data-ttu-id="8122b-311">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8122b-311">Requirement</span></span> | <span data-ttu-id="8122b-312">Wert</span><span class="sxs-lookup"><span data-stu-id="8122b-312">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8122b-313">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8122b-313">Minimum supported client</span></span><br/> | <span data-ttu-id="8122b-314">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8122b-314">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8122b-315">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8122b-315">Minimum supported server</span></span><br/> | <span data-ttu-id="8122b-316">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8122b-316">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8122b-317">Namespace</span><span class="sxs-lookup"><span data-stu-id="8122b-317">Namespace</span></span><br/>                | <span data-ttu-id="8122b-318">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8122b-318">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8122b-319">MOF</span><span class="sxs-lookup"><span data-stu-id="8122b-319">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8122b-320"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8122b-320"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8122b-321">DLL</span><span class="sxs-lookup"><span data-stu-id="8122b-321">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8122b-322"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8122b-322"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8122b-323">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8122b-323">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8122b-324">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="8122b-324">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

