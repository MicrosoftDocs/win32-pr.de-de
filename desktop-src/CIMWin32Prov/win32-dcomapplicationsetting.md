---
description: Win32 \_ dcomapplicationsetting&\# 8194; Die WMI-Klasse stellt die Einstellungen einer DCOM-Anwendung dar.
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Win32_DCOMApplicationSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343019"
---
# <a name="win32_dcomapplicationsetting-class"></a><span data-ttu-id="f4f05-103">Win32 \_ dcomapplicationsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="f4f05-103">Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="f4f05-104">Die **Win32 \_ dcomapplicationsetting** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Einstellungen einer DCOM-Anwendung dar.</span><span class="sxs-lookup"><span data-stu-id="f4f05-104">The **Win32\_DCOMApplicationSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a DCOM application.</span></span> <span data-ttu-id="f4f05-105">Sie enthält DCOM-Konfigurationsoptionen, die mit dem **AppID** -Schlüssel in der Registrierung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f4f05-105">It contains DCOM configuration options associated with the **AppID** key in the registry.</span></span> <span data-ttu-id="f4f05-106">Diese Optionen sind für die Komponenten gültig, die logisch unter der angegebenen Anwendungsklasse gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="f4f05-106">These options are valid on the components logically grouped under the given application class.</span></span>

<span data-ttu-id="f4f05-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f4f05-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f4f05-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f4f05-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f05-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4f05-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a><span data-ttu-id="f4f05-110">Member</span><span class="sxs-lookup"><span data-stu-id="f4f05-110">Members</span></span>

<span data-ttu-id="f4f05-111">Die **Win32 \_ dcomapplicationsetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f4f05-111">The **Win32\_DCOMApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f4f05-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f4f05-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f4f05-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4f05-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f4f05-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="f4f05-114">Methods</span></span>

<span data-ttu-id="f4f05-115">Die **Win32 \_ dcomapplicationsetting** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f4f05-115">The **Win32\_DCOMApplicationSetting** class has these methods.</span></span>



| <span data-ttu-id="f4f05-116">Methode</span><span class="sxs-lookup"><span data-stu-id="f4f05-116">Method</span></span>                                                                                                                        | <span data-ttu-id="f4f05-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4f05-117">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4f05-118">**Getaccesssecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="f4f05-118">**GetAccessSecurityDescriptor**</span></span>](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="f4f05-119">Ruft die Sicherheits Beschreibung ab, die steuert, wer auf eine DCOM-Anwendung zugreifen darf.</span><span class="sxs-lookup"><span data-stu-id="f4f05-119">Gets the security descriptor that controls who is allowed to access a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="f4f05-120">**Getconfigurationsecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="f4f05-120">**GetConfigurationSecurityDescriptor**</span></span>](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="f4f05-121">Ruft die Sicherheits Beschreibung ab, die steuert, wer eine DCOM-Anwendung konfigurieren darf.</span><span class="sxs-lookup"><span data-stu-id="f4f05-121">Gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="f4f05-122">**Getlaunchsecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="f4f05-122">**GetLaunchSecurityDescriptor**</span></span>](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | <span data-ttu-id="f4f05-123">Ruft die Sicherheits Beschreibung ab, die steuert, wer eine DCOM-Anwendung starten darf.</span><span class="sxs-lookup"><span data-stu-id="f4f05-123">Gets the security descriptor that controls who is allowed to launch a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="f4f05-124">**Setaccesssecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="f4f05-124">**SetAccessSecurityDescriptor**</span></span>](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="f4f05-125">Aktualisiert den Zugriffs Sicherheits Deskriptor der DCOM-Anwendung mit einer neuen Sicherheits Beschreibung, die durch eine Instanz der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f4f05-125">Updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |
| [<span data-ttu-id="f4f05-126">**Setconfigurationsecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="f4f05-126">**SetConfigurationSecurityDescriptor**</span></span>](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="f4f05-127">Aktualisiert die Konfigurations Sicherheits Beschreibung der DCOM-Anwendung mit einer neuen Sicherheits Beschreibung, die durch eine Instanz der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f4f05-127">Updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/> |
| [<span data-ttu-id="f4f05-128">**Setlaunchsecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="f4f05-128">**SetLaunchSecurityDescriptor**</span></span>](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="f4f05-129">Aktualisiert die Start Sicherheits Beschreibung der DCOM-Anwendung mit einer neuen Sicherheits Beschreibung, die durch eine Instanz der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f4f05-129">Updates the launch security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="f4f05-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4f05-130">Properties</span></span>

<span data-ttu-id="f4f05-131">Die **Win32 \_ dcomapplicationsetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f4f05-131">The **Win32\_DCOMApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4f05-132">**AppID**</span><span class="sxs-lookup"><span data-stu-id="f4f05-132">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4f05-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4f05-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-135">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="f4f05-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-136">GUID (Global Unique Identifier) für diese DCOM-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f4f05-136">Globally unique identifier (GUID) for this DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-137">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="f4f05-137">**AuthenticationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4f05-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4f05-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-140">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")</span><span class="sxs-lookup"><span data-stu-id="f4f05-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[AuthenticationLevel\]")</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-141">Mindestens erforderliche Client Authentifizierungs Ebene für diesen com-Server.</span><span class="sxs-lookup"><span data-stu-id="f4f05-141">Minimum client authentication level required by this COM server.</span></span> <span data-ttu-id="f4f05-142">Wenn der Wert **null** ist, werden die Standardwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4f05-142">If **NULL**, the default values are used.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="f4f05-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (1)</span><span class="sxs-lookup"><span data-stu-id="f4f05-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f4f05-144">None (keine Authentifizierung erfolgt)</span><span class="sxs-lookup"><span data-stu-id="f4f05-144">None (no authentication is performed)</span></span>

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span data-ttu-id="f4f05-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Verbinden** (2)</span><span class="sxs-lookup"><span data-stu-id="f4f05-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connect** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f4f05-146">Connect (die Authentifizierung wird nur ausgeführt, wenn der Client eine Beziehung mit der Anwendung herstellt)</span><span class="sxs-lookup"><span data-stu-id="f4f05-146">Connect (authentication is performed only when the client establishes a relationship with the application)</span></span>

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span data-ttu-id="f4f05-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Rückruf** (3)</span><span class="sxs-lookup"><span data-stu-id="f4f05-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Call** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f4f05-148">Wird aufgerufen (die Authentifizierung wird nur zu Beginn jedes Aufrufes ausgeführt, wenn die Anwendung die Anforderung empfängt)</span><span class="sxs-lookup"><span data-stu-id="f4f05-148">Call (authentication is performed only at the beginning of each call when the application receives the request)</span></span>

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span data-ttu-id="f4f05-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Paket** (4)</span><span class="sxs-lookup"><span data-stu-id="f4f05-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Packet** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f4f05-150">Paket (Authentifizierung wird für alle vom Client empfangenen Daten ausgeführt)</span><span class="sxs-lookup"><span data-stu-id="f4f05-150">Packet (authentication is performed on all of the data received from the client)</span></span>

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span data-ttu-id="f4f05-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**Packetintegrity** (5)</span><span class="sxs-lookup"><span data-stu-id="f4f05-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f4f05-152">Packetintegrity (alle Daten, die zwischen dem Client und der Anwendung übertragen werden, werden authentifiziert und überprüft.)</span><span class="sxs-lookup"><span data-stu-id="f4f05-152">PacketIntegrity (all of the data transferred between the client and the application is authenticated and verified)</span></span>

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span data-ttu-id="f4f05-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span><span class="sxs-lookup"><span data-stu-id="f4f05-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f4f05-154">PacketPrivacy (die Eigenschaften der anderen Authentifizierungs Ebenen werden verwendet, und alle Daten werden verschlüsselt.)</span><span class="sxs-lookup"><span data-stu-id="f4f05-154">PacketPrivacy (the properties of the other authentication levels are used and all of the data is encrypted)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f4f05-155">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f4f05-155">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4f05-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4f05-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-158">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f4f05-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-159">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f4f05-159">Short textual description of the current object.</span></span>

<span data-ttu-id="f4f05-160">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f4f05-160">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-161">**Customersatz**</span><span class="sxs-lookup"><span data-stu-id="f4f05-161">**CustomSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4f05-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4f05-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-164">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ dllersatz \] ")</span><span class="sxs-lookup"><span data-stu-id="f4f05-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-165">Der Name des benutzerdefinierten Ersatz Zeichens, in dem die Prozess interne DCOM-Anwendung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f4f05-165">Name of the custom surrogate in which the in-process DCOM application is activated.</span></span> <span data-ttu-id="f4f05-166">Wenn dieser Wert **null** ist und der **UseSurrogate** -Schlüssel auf **true** festgelegt ist, stellt das System einen Ersatzprozess bereit.</span><span class="sxs-lookup"><span data-stu-id="f4f05-166">If this value is **NULL** and the **UseSurrogate** key is **TRUE**, then the system provides a surrogate process.</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-167">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4f05-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4f05-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4f05-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-170">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f4f05-170">Textual description of the current object.</span></span>

<span data-ttu-id="f4f05-171">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f4f05-171">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-172">**EnableAtStorageActivation**</span><span class="sxs-lookup"><span data-stu-id="f4f05-172">**EnableAtStorageActivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-173">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f4f05-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4f05-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-175">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ activateatstorage \] ")</span><span class="sxs-lookup"><span data-stu-id="f4f05-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ActivateAtStorage\]")</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-176">Die DCOM-Anwendung ruft den gespeicherten Zustand der Anwendung ab oder beginnt mit dem Zustand, in dem die Anwendung zuerst initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f4f05-176">DCOM application retrieves the saved state of the application or begins from the state in which the application is first initialized.</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-177">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="f4f05-177">**LocalService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4f05-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4f05-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-180">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")</span><span class="sxs-lookup"><span data-stu-id="f4f05-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[LocalService\]")</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-181">Der Name der Dienste, die von der DCOM-Anwendung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f4f05-181">Name for the services provided by the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-182">**RemoteServerName**</span><span class="sxs-lookup"><span data-stu-id="f4f05-182">**RemoteServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4f05-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-184">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4f05-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-185">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ Remoteservername \] ")</span><span class="sxs-lookup"><span data-stu-id="f4f05-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RemoteServerName\]")</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-186">Der Name des Remote Servers, auf dem die Anwendung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f4f05-186">Name of the remote server where the application is activated.</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-187">**RunAsUser**</span><span class="sxs-lookup"><span data-stu-id="f4f05-187">**RunAsUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4f05-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4f05-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-190">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ runas \] ")</span><span class="sxs-lookup"><span data-stu-id="f4f05-190">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RunAs\]")</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-191">Bestimmtes Benutzerkonto, unter dem die Anwendung bei Aktivierung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4f05-191">Specific user account under which the application is to be run on activation.</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-192">**Service Parameters**</span><span class="sxs-lookup"><span data-stu-id="f4f05-192">**ServiceParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4f05-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4f05-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-195">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ Service Parameters \] ")</span><span class="sxs-lookup"><span data-stu-id="f4f05-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ServiceParameters\]")</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-196">Befehlszeilenparameter, die an die DCOM-Anwendung übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="f4f05-196">Command-line parameters passed to the DCOM application.</span></span> <span data-ttu-id="f4f05-197">Dies ist nur gültig, wenn die Anwendung als Windows-basierter Dienst geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f4f05-197">This is valid only if the application is written as a Windows-based service.</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-198">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="f4f05-198">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4f05-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4f05-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-201">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f4f05-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-202">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="f4f05-202">Identifier by which the current object is known.</span></span>

<span data-ttu-id="f4f05-203">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f4f05-203">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4f05-204">**UseSurrogate**</span><span class="sxs-lookup"><span data-stu-id="f4f05-204">**UseSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4f05-205">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f4f05-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-206">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f4f05-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f4f05-207">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ dllersatz \] ")</span><span class="sxs-lookup"><span data-stu-id="f4f05-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="f4f05-208">Die DCOM-Anwendung kann als Prozess interner Server aktiviert werden, indem eine ausführbare Datei für Ersatz Zeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4f05-208">DCOM application can be activated as an out-of-process server by use of a surrogate executable file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4f05-209">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4f05-209">Remarks</span></span>

<span data-ttu-id="f4f05-210">Die **Win32 \_ dcomapplicationsetting** -Klasse wird von [**Win32 \_ comsetting**](win32-comsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f4f05-210">The **Win32\_DCOMApplicationSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f05-211">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4f05-211">Requirements</span></span>



| <span data-ttu-id="f4f05-212">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4f05-212">Requirement</span></span> | <span data-ttu-id="f4f05-213">Wert</span><span class="sxs-lookup"><span data-stu-id="f4f05-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f05-214">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4f05-214">Minimum supported client</span></span><br/> | <span data-ttu-id="f4f05-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4f05-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4f05-216">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4f05-216">Minimum supported server</span></span><br/> | <span data-ttu-id="f4f05-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4f05-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4f05-218">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4f05-218">Namespace</span></span><br/>                | <span data-ttu-id="f4f05-219">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f4f05-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f4f05-220">MOF</span><span class="sxs-lookup"><span data-stu-id="f4f05-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4f05-221"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f4f05-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4f05-222">DLL</span><span class="sxs-lookup"><span data-stu-id="f4f05-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4f05-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4f05-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f05-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4f05-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f05-225">**Win32- \_ comsetting**</span><span class="sxs-lookup"><span data-stu-id="f4f05-225">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="f4f05-226">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4f05-226">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f4f05-227">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="f4f05-227">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="f4f05-228">WMI-sicherheitsdeskriptorobjekte</span><span class="sxs-lookup"><span data-stu-id="f4f05-228">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="f4f05-229">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="f4f05-229">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

