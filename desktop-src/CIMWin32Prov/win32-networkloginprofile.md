---
description: Das Win32- \_ networkloginprofile-&\# 8194; Die WMI-Klasse stellt die Netzwerk Anmelde Informationen eines bestimmten Benutzers auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Win32_NetworkLoginProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b138ce4bc92088896286f4a21a039b068e2206e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343005"
---
# <a name="win32_networkloginprofile-class"></a><span data-ttu-id="67bab-103">Win32 \_ networkloginprofile-Klasse</span><span class="sxs-lookup"><span data-stu-id="67bab-103">Win32\_NetworkLoginProfile class</span></span>

<span data-ttu-id="67bab-104">Die **Win32 \_ networkloginprofile**- [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt die Netzwerk Anmelde Informationen eines bestimmten Benutzers auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67bab-104">The **Win32\_NetworkLoginProfile** [WMI class](../wmisdk/retrieving-a-class.md) represents the network login information of a specific user on a computer system running Windows.</span></span> <span data-ttu-id="67bab-105">Dies umfasst u. a. den Kenn Wort Status, Zugriffsrechte, Datenträger Kontingente und Anmelde Verzeichnispfade.</span><span class="sxs-lookup"><span data-stu-id="67bab-105">This includes, but is not limited to password status, access privileges, disk quotas, and logon directory paths.</span></span>

<span data-ttu-id="67bab-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="67bab-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67bab-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="67bab-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a><span data-ttu-id="67bab-108">Member</span><span class="sxs-lookup"><span data-stu-id="67bab-108">Members</span></span>

<span data-ttu-id="67bab-109">Die **Win32 \_ networkloginprofile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="67bab-109">The **Win32\_NetworkLoginProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="67bab-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67bab-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67bab-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67bab-111">Properties</span></span>

<span data-ttu-id="67bab-112">Die **Win32 \_ networkloginprofile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="67bab-112">The **Win32\_NetworkLoginProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67bab-113">**AccountExpires**</span><span class="sxs-lookup"><span data-stu-id="67bab-113">**AccountExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-114">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="67bab-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-116">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Acct \_ läuft ab")</span><span class="sxs-lookup"><span data-stu-id="67bab-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_acct\_expires")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-117">Das Konto läuft ab.</span><span class="sxs-lookup"><span data-stu-id="67bab-117">Account will expire.</span></span> <span data-ttu-id="67bab-118">Dieser Wert wird anhand der Anzahl der seit 00:00:00, dem 1. Januar 1970 verstrichenen Sekunden berechnet und im folgenden Format festgelegt: YYYYMMDDHHMMSS. mmmmmm sutc.</span><span class="sxs-lookup"><span data-stu-id="67bab-118">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970, and is set in this format: yyyymmddhhmmss.mmmmmm sutc.</span></span>

<span data-ttu-id="67bab-119">Beispiel: 20521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="67bab-119">Example: 20521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="67bab-120">**Authorizationflags**</span><span class="sxs-lookup"><span data-stu-id="67bab-120">**AuthorizationFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-121">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-123">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Authentifizierung \_ Flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span><span class="sxs-lookup"><span data-stu-id="67bab-123">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_auth\_flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-124">Ein Satz von Flags, die die Ressourcen angeben, die ein Benutzer für die Verwendung oder Änderung autorisiert ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-124">Set of flags that specify the resources a user is authorized to use or modify.</span></span>

<dt>

<span data-ttu-id="67bab-125">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="67bab-125">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-126">Drucker</span><span class="sxs-lookup"><span data-stu-id="67bab-126">Printer</span></span>

</dd> <dt>

<span data-ttu-id="67bab-127">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="67bab-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-128">Kommunikation</span><span class="sxs-lookup"><span data-stu-id="67bab-128">Communication</span></span>

</dd> <dt>

<span data-ttu-id="67bab-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="67bab-129">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-130">Server</span><span class="sxs-lookup"><span data-stu-id="67bab-130">Server</span></span>

</dd> <dt>

<span data-ttu-id="67bab-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="67bab-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-132">Konten</span><span class="sxs-lookup"><span data-stu-id="67bab-132">Accounts</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67bab-133">**BadPasswordCount**</span><span class="sxs-lookup"><span data-stu-id="67bab-133">**BadPasswordCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-136">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| nettuserenum")</span><span class="sxs-lookup"><span data-stu-id="67bab-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|NetUserEnum")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-137">Gibt an, wie oft der Benutzer ein ungültiges Kennwort eingibt, wenn er sich bei einem Computersystem mit Windows anmeldet.</span><span class="sxs-lookup"><span data-stu-id="67bab-137">Number of times the user enters a bad password when logging on to a computer system running Windows.</span></span>

<span data-ttu-id="67bab-138">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="67bab-138">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="67bab-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="67bab-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-142">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="67bab-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="67bab-143">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="67bab-143">Short textual description of the current object.</span></span>

<span data-ttu-id="67bab-144">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="67bab-144">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="67bab-145">**CodePage**</span><span class="sxs-lookup"><span data-stu-id="67bab-145">**CodePage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-148">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ Codepage")</span><span class="sxs-lookup"><span data-stu-id="67bab-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_code\_page")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-149">Codepage für die Sprache des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="67bab-149">Code page for the user's language of choice.</span></span> <span data-ttu-id="67bab-150">Eine Codepage ist der verwendete Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="67bab-150">A code page is the character set used.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-151">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="67bab-151">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-154">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ comment")</span><span class="sxs-lookup"><span data-stu-id="67bab-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-155">Kommentar oder Beschreibung für dieses Anmelde Profil.</span><span class="sxs-lookup"><span data-stu-id="67bab-155">Comment or description for this logon profile.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-156">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="67bab-156">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-159">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Country \_ Code")</span><span class="sxs-lookup"><span data-stu-id="67bab-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_country\_code")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-160">Länder-/Regionscode für die Sprache des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="67bab-160">Country/region code for the user's language of choice.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67bab-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67bab-164">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="67bab-164">Textual description of the current object.</span></span>

<span data-ttu-id="67bab-165">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="67bab-165">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="67bab-166">**Flags**</span><span class="sxs-lookup"><span data-stu-id="67bab-166">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-167">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-169">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags"), [**Bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account deaktiviert", "Home dir erforderlich", "Lock out", "password not required", "paswword nicht ändern", "verschlüsseltes Testkennwort zulässig", "temporäres doppeltes Konto", "normales Konto", "Konto für Domänen übergreifende Vertrauensstellung" "," Arbeitsstations-Vertrauensstellungs Konto "," Server Vertrauensstellungs Konto "," Kennwort nicht ablaufen "," MNS-Anmelde Konto "," Smartcard erforderlich "," vertrauenswürdig für Delegierung "," nicht delegiert "," nur den Schlüssel verwenden "," keine vorab Autorisierung erforderlich "," Kennwort abgelaufen ")</span><span class="sxs-lookup"><span data-stu-id="67bab-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account Disabled", "Home Dir Required", "Lockout", "Password Not Required", "Paswword Can't Change", "Encrypted Test Password Allowed", "Temp Duplicate Account", "Normal Account", "InterDomain Trust Account", "WorkStation Trust Account", "Server Trust Account", "Don't Expire Password", "MNS Logon Account", "Smartcard Required", "Trusted For Delegation", "Not Delegated", "Use DES Key Only", "Don't Require Preauthorization", "Password Expired")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-170">Die Eigenschaften, die für dieses Netzwerk Profil verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="67bab-170">The properties available to this network profile.</span></span>

<span data-ttu-id="67bab-171">Folgende Eigenschaften können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="67bab-171">Properties that can be set include:</span></span>

<dt>

<span data-ttu-id="67bab-172">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="67bab-172">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-173">Skript</span><span class="sxs-lookup"><span data-stu-id="67bab-173">Script</span></span>

<span data-ttu-id="67bab-174">Ein ausgeführtes Anmelde Skript.</span><span class="sxs-lookup"><span data-stu-id="67bab-174">A logon script executed.</span></span> <span data-ttu-id="67bab-175">Dieser Wert muss für den LAN-Manager 2,0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="67bab-175">This value must be set for LAN Manager 2.0.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-176">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="67bab-176">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-177">Konto deaktiviert</span><span class="sxs-lookup"><span data-stu-id="67bab-177">Account Disabled</span></span>

<span data-ttu-id="67bab-178">Das Konto des Benutzers ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="67bab-178">The user's account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-179">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="67bab-179">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-180">Basisverzeichnis erforderlich</span><span class="sxs-lookup"><span data-stu-id="67bab-180">Home Directory Required</span></span>

<span data-ttu-id="67bab-181">Ein Basisverzeichnis ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="67bab-181">A home directory is required.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-182">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="67bab-182">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-183">Sperrung</span><span class="sxs-lookup"><span data-stu-id="67bab-183">Lockout</span></span>

<span data-ttu-id="67bab-184">Das Konto ist zurzeit gesperrt. Für " [**nettusersetinfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo)" kann dieser Wert gelöscht werden, um ein zuvor gesperrtes Konto zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="67bab-184">The account is currently locked out. For [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), this value can be cleared to unlock a previously locked account.</span></span> <span data-ttu-id="67bab-185">Dieser Wert kann nicht verwendet werden, um ein zuvor entsperrtes Konto zu sperren.</span><span class="sxs-lookup"><span data-stu-id="67bab-185">This value cannot be used to lock a previously unlocked account.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-186">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="67bab-186">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-187">Kennwort nicht erforderlich</span><span class="sxs-lookup"><span data-stu-id="67bab-187">Password Not Required</span></span>

<span data-ttu-id="67bab-188">Es ist kein Kennwort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="67bab-188">No password is required.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-189">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="67bab-189">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-190">Kenn Wort Änderung nicht möglich</span><span class="sxs-lookup"><span data-stu-id="67bab-190">Password Cannot Change</span></span>

<span data-ttu-id="67bab-191">Der Benutzer kann das Kennwort nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="67bab-191">The user cannot change the password.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-192">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="67bab-192">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-193">Verschlüsseltes Testkennwort zulässig</span><span class="sxs-lookup"><span data-stu-id="67bab-193">Encrypted Test Password Allowed</span></span>

</dd> <dt>

<span data-ttu-id="67bab-194">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="67bab-194">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-195">Temporäres doppeltes Konto</span><span class="sxs-lookup"><span data-stu-id="67bab-195">Temp Duplicate Account</span></span>

<span data-ttu-id="67bab-196">Ein Konto für Benutzer, deren primäres Konto sich in einer anderen Domäne befindet.</span><span class="sxs-lookup"><span data-stu-id="67bab-196">An account for users whose primary account is in another domain.</span></span> <span data-ttu-id="67bab-197">Dieses Konto ermöglicht dem Benutzer den Zugriff auf diese Domäne, jedoch nicht auf eine Domäne, die dieser Domäne vertraut.</span><span class="sxs-lookup"><span data-stu-id="67bab-197">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="67bab-198">Der Benutzer-Manager verweist auf diesen Kontotyp als lokales Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="67bab-198">The User Manager refers to this account type as a local user account.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-199">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="67bab-199">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-200">Normales Konto</span><span class="sxs-lookup"><span data-stu-id="67bab-200">Normal Account</span></span>

<span data-ttu-id="67bab-201">Der Standard Kontotyp, der einen typischen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="67bab-201">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-202">2048 (0x800)</span><span class="sxs-lookup"><span data-stu-id="67bab-202">2048 (0x800)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-203">Konto für Domänen übergreifende Vertrauensstellung</span><span class="sxs-lookup"><span data-stu-id="67bab-203">Interdomain Trust Account</span></span>

<span data-ttu-id="67bab-204">Eine Zulassungsberechtigung für ein Vertrauensstellungs Konto für eine Domäne, die anderen Domänen vertraut.</span><span class="sxs-lookup"><span data-stu-id="67bab-204">A permit to a trust account for a domain that trusts other domains.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-205">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="67bab-205">4096 (0x1000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-206">Arbeitsstations-Vertrauens Konto</span><span class="sxs-lookup"><span data-stu-id="67bab-206">Workstation Trust Account</span></span>

<span data-ttu-id="67bab-207">Ein Computer Konto für eine Windows-Arbeitsstation oder einen Server, das Mitglied dieser Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-207">A computer account for a Windows workstation or server that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-208">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="67bab-208">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-209">Server Vertrauensstellungs Konto</span><span class="sxs-lookup"><span data-stu-id="67bab-209">Server Trust Account</span></span>

<span data-ttu-id="67bab-210">Ein Computer Konto für einen Sicherungs Domänen Controller, der Mitglied dieser Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-210">A computer account for a backup domain controller that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-211">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="67bab-211">65536 (0x10000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-212">Kennwort nicht ablaufen</span><span class="sxs-lookup"><span data-stu-id="67bab-212">Do Not Expire Password</span></span>

</dd> <dt>

<span data-ttu-id="67bab-213">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="67bab-213">131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-214">MNS-Anmelde Konto</span><span class="sxs-lookup"><span data-stu-id="67bab-214">MNS Logon Account</span></span>

<span data-ttu-id="67bab-215">MNS-Anmelde Kontotyp (Majority Node Set), der einen MNS-Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="67bab-215">Majority Node Set (MNS) logon account type that represents an MNS user.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-216">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="67bab-216">262144 (0x40000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-217">Smartcard erforderlich</span><span class="sxs-lookup"><span data-stu-id="67bab-217">Smartcard Required</span></span>

</dd> <dt>

<span data-ttu-id="67bab-218">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="67bab-218">524288 (0x80000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-219">Vertrauenswürdige Delegierung</span><span class="sxs-lookup"><span data-stu-id="67bab-219">Trusted for Delegation</span></span>

</dd> <dt>

<span data-ttu-id="67bab-220">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="67bab-220">1048576 (0x100000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-221">Nicht delegiert</span><span class="sxs-lookup"><span data-stu-id="67bab-221">Not Delegated</span></span>

</dd> <dt>

<span data-ttu-id="67bab-222">2097152 (0x200.000)</span><span class="sxs-lookup"><span data-stu-id="67bab-222">2097152 (0x200000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-223">Nur des-Schlüssels verwenden</span><span class="sxs-lookup"><span data-stu-id="67bab-223">Use DES Key Only</span></span>

</dd> <dt>

<span data-ttu-id="67bab-224">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="67bab-224">4194304 (0x400000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-225">Keine vorab Autorisierung erforderlich</span><span class="sxs-lookup"><span data-stu-id="67bab-225">Do Not Require Preauthorization</span></span>

</dd> <dt>

<span data-ttu-id="67bab-226">8388608 (0x800000)</span><span class="sxs-lookup"><span data-stu-id="67bab-226">8388608 (0x800000)</span></span>
</dt> <dd>

<span data-ttu-id="67bab-227">Kennwort abgelaufen</span><span class="sxs-lookup"><span data-stu-id="67bab-227">Password Expired</span></span>

<span data-ttu-id="67bab-228">Gibt an, dass das Kennwort abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-228">Indicates that the password has expired.</span></span>

</dd> </dl>

<span data-ttu-id="67bab-229">Die folgenden Eigenschaften beschreiben den Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="67bab-229">The following properties describe the account type.</span></span> <span data-ttu-id="67bab-230">Es kann nur ein Wert festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="67bab-230">Only one value can be set:</span></span>

-   <span data-ttu-id="67bab-231">\_normales \_ Konto</span><span class="sxs-lookup"><span data-stu-id="67bab-231">UF\_NORMAL\_ACCOUNT</span></span>
-   <span data-ttu-id="67bab-232">\_Konto für Temp Temp- \_ Duplizierung \_</span><span class="sxs-lookup"><span data-stu-id="67bab-232">UF\_TEMP\_DUPLICATE\_ACCOUNT</span></span>
-   <span data-ttu-id="67bab-233">Konto der Vertrauensstellung der \_ \_ Vertrauensstellung \_</span><span class="sxs-lookup"><span data-stu-id="67bab-233">UF\_WORKSTATION\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="67bab-234">\_ \_ \_ Konto Vertrauens Konto für den Server</span><span class="sxs-lookup"><span data-stu-id="67bab-234">UF\_SERVER\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="67bab-235">Konto für die Vertrauensstellung der \_ Verbindungs Domäne \_ \_</span><span class="sxs-lookup"><span data-stu-id="67bab-235">UF\_INTERDOMAIN\_TRUST\_ACCOUNT</span></span>

</dd> <dt>

<span data-ttu-id="67bab-236">**FullName**</span><span class="sxs-lookup"><span data-stu-id="67bab-236">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-239">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Full \_ Name")</span><span class="sxs-lookup"><span data-stu-id="67bab-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_full\_name")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-240">Der vollständige Name des Benutzers, der zum Netzwerk Anmelde Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="67bab-240">Full name of the user belonging to the network login profile.</span></span> <span data-ttu-id="67bab-241">Diese Zeichenfolge kann leer sein, wenn der Benutzer keinen vollständigen Namen mit einem Benutzernamen zuordnen möchte.</span><span class="sxs-lookup"><span data-stu-id="67bab-241">This string can be empty if the user chooses not to associate a full name with a user name.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-242">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="67bab-242">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-243">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-245">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir")</span><span class="sxs-lookup"><span data-stu-id="67bab-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-246">Pfad zum Basisverzeichnis des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="67bab-246">Path to the home directory of the user.</span></span> <span data-ttu-id="67bab-247">Diese Zeichenfolge ist möglicherweise leer, wenn der Benutzer kein Basisverzeichnis angeben möchte.</span><span class="sxs-lookup"><span data-stu-id="67bab-247">This string may be empty if the user chooses not to specify a home directory.</span></span>

<span data-ttu-id="67bab-248">Beispiel: " \\ homedir"</span><span class="sxs-lookup"><span data-stu-id="67bab-248">Example:"\\HOMEDIR"</span></span>

</dd> <dt>

<span data-ttu-id="67bab-249">**Homedirectorydrive**</span><span class="sxs-lookup"><span data-stu-id="67bab-249">**HomeDirectoryDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-250">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-252">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir \_ Drive")</span><span class="sxs-lookup"><span data-stu-id="67bab-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir\_drive")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-253">Laufwerk Buchstabe, der dem Basisverzeichnis des Benutzers für die Anmeldung zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="67bab-253">Drive letter assigned to the user's home directory for log on purposes.</span></span>

<span data-ttu-id="67bab-254">Beispiel: "C:"</span><span class="sxs-lookup"><span data-stu-id="67bab-254">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="67bab-255">**Lastlogoff**</span><span class="sxs-lookup"><span data-stu-id="67bab-255">**LastLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-256">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="67bab-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-258">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Logoff")</span><span class="sxs-lookup"><span data-stu-id="67bab-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logoff")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-259">Der Benutzer hat das System zuletzt abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="67bab-259">User last logged off the system.</span></span> <span data-ttu-id="67bab-260">Dieser Wert wird anhand der Anzahl der Sekunden berechnet, die seit 00:00:00, dem 1. Januar 1970, verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="67bab-260">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="67bab-261">Der Wert " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " bedeutet, dass die letzte Abmelde Zeit unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-261">A value of " \*\*\*\*\*\*\*\*\*\*\*\*\*\*.\*\*\*\*\*\*+\*\*\* " means that the last logoff time is unknown.</span></span> <span data-ttu-id="67bab-262">Das Format dieses Werts lautet YYYYMMDDHHMMSS. mmmmmm sutc.</span><span class="sxs-lookup"><span data-stu-id="67bab-262">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="67bab-263">Informationen zum übersetzen dieser Eigenschaft in die Ortszeit finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="67bab-263">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="67bab-264">Beispiel: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="67bab-264">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="67bab-265">**LastLogon**</span><span class="sxs-lookup"><span data-stu-id="67bab-265">**LastLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-266">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="67bab-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-268">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Last \_ Login")</span><span class="sxs-lookup"><span data-stu-id="67bab-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logon")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-269">Der Benutzer hat sich zuletzt am System angemeldet.</span><span class="sxs-lookup"><span data-stu-id="67bab-269">User last logged on to the system.</span></span> <span data-ttu-id="67bab-270">Dieser Wert wird anhand der Anzahl der Sekunden berechnet, die seit 00:00:00, dem 1. Januar 1970, verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="67bab-270">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="67bab-271">Das Format dieses Werts lautet YYYYMMDDHHMMSS. mmmmmm sutc.</span><span class="sxs-lookup"><span data-stu-id="67bab-271">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="67bab-272">Informationen zum übersetzen dieser Eigenschaft in die Ortszeit finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="67bab-272">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="67bab-273">Beispiel: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="67bab-273">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="67bab-274">**LogonHours**</span><span class="sxs-lookup"><span data-stu-id="67bab-274">**LogonHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-275">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-277">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (147), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Hours")</span><span class="sxs-lookup"><span data-stu-id="67bab-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_hours")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-278">Die Zeiten in der Woche, an denen sich der Benutzer anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="67bab-278">Times during the week when the user can log on.</span></span> <span data-ttu-id="67bab-279">Jedes Bit stellt eine Zeiteinheit dar, die durch die **UnitsPerWeek** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="67bab-279">Each bit represents a unit of time specified by the **UnitsPerWeek** property.</span></span> <span data-ttu-id="67bab-280">Wenn beispielsweise die Zeiteinheit stündlich ist, ist das erste Bit (Bit 0, Wort 0) Sonntag, 0:00 bis 0:59, das zweite Bit (Bit 1, Wort 0) ist Sonntag, 1:00 bis 1:59 usw.</span><span class="sxs-lookup"><span data-stu-id="67bab-280">For instance, if the unit of time is hourly, the first bit (bit 0, word 0) is Sunday, 0:00 to 0:59, the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59, and so on.</span></span> <span data-ttu-id="67bab-281">Wenn dieser Member auf **null** festgelegt ist, gibt es keine Zeitbeschränkung.</span><span class="sxs-lookup"><span data-stu-id="67bab-281">If this member is set to **NULL**, then there is no time restriction.</span></span> <span data-ttu-id="67bab-282">Die Uhrzeit wird auf GMT festgelegt und muss für andere Zeitzonen angepasst werden (z. b. GMT minus 8 Stunden für PST).</span><span class="sxs-lookup"><span data-stu-id="67bab-282">The time is set to GMT and must be adjusted for other time zones (for example, GMT minus 8 hours for PST).</span></span>

</dd> <dt>

<span data-ttu-id="67bab-283">**LOGONSERVER**</span><span class="sxs-lookup"><span data-stu-id="67bab-283">**LogonServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-284">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-286">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Server")</span><span class="sxs-lookup"><span data-stu-id="67bab-286">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_server")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-287">Der Name des Servers, an den Anmelde Anforderungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="67bab-287">Name of the server to which logon requests are sent.</span></span> <span data-ttu-id="67bab-288">Server Namen sollten zwei umgekehrte Schrägstriche () vorangestellt werden \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="67bab-288">Server names should be preceded by two backslashes (\\\\).</span></span> <span data-ttu-id="67bab-289">Ein Servername mit einem Sternchen ( \\ \\ \* ) gibt an, dass die Anmelde Anforderung von jedem beliebigen Anmelde Server verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="67bab-289">A server name with an asterisk (\\\\\*) indicates that the logon request can be handled by any logon server.</span></span> <span data-ttu-id="67bab-290">Eine NULL-Zeichenfolge gibt an, dass Anforderungen an den Domänen Controller gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="67bab-290">A null string indicates that requests are sent to the domain controller.</span></span>

<span data-ttu-id="67bab-291">Beispiel: " \\ \\ myserver"</span><span class="sxs-lookup"><span data-stu-id="67bab-291">Example: "\\\\MyServer"</span></span>

</dd> <dt>

<span data-ttu-id="67bab-292">**MaximumStorage**</span><span class="sxs-lookup"><span data-stu-id="67bab-292">**MaximumStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-293">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67bab-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-295">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ Storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="67bab-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_max\_storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-296">Maximale Menge an Speicherplatz, die dem Benutzer zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="67bab-296">Maximum amount of disk space available to the user.</span></span> <span data-ttu-id="67bab-297">Wenn MaximumStorage auf User \_ maxstorage Unlimited festgelegt ist \_ , darf der Benutzer den gesamten verfügbaren Speicherplatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="67bab-297">If MaximumStorage is set to USER\_MAXSTORAGE\_UNLIMITED, the user is allowed to use all of the available disk space.</span></span>

<span data-ttu-id="67bab-298">Beispiel: 10 Millionen</span><span class="sxs-lookup"><span data-stu-id="67bab-298">Example: 10000000</span></span>

<span data-ttu-id="67bab-299">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67bab-299">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67bab-300">**Name**</span><span class="sxs-lookup"><span data-stu-id="67bab-300">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-303">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Name")</span><span class="sxs-lookup"><span data-stu-id="67bab-303">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_name")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-304">Benutzerkonto für eine bestimmte Domäne oder einen bestimmten Computer.</span><span class="sxs-lookup"><span data-stu-id="67bab-304">User account on a particular domain or computer.</span></span> <span data-ttu-id="67bab-305">Die Anzahl der Zeichen im Namen darf den Wert von UNLEN nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="67bab-305">The number of characters in the name cannot exceed the value of UNLEN.</span></span>

<span data-ttu-id="67bab-306">Beispiel: "somedomäne \\ JohnDoe"</span><span class="sxs-lookup"><span data-stu-id="67bab-306">Example: "somedomain\\johndoe"</span></span>

</dd> <dt>

<span data-ttu-id="67bab-307">**Anzahloflogone**</span><span class="sxs-lookup"><span data-stu-id="67bab-307">**NumberOfLogons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-308">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-310">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ NUM \_ Logons")</span><span class="sxs-lookup"><span data-stu-id="67bab-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_num\_logons")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-311">Gibt an, wie oft der Benutzer versucht hat, sich bei diesem Konto anzumelden.</span><span class="sxs-lookup"><span data-stu-id="67bab-311">Number of successful times the user tried to log on to this account.</span></span> <span data-ttu-id="67bab-312">Der Wert 0xFFFFFFFF gibt an, dass der Wert unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-312">A value of 0xFFFFFFFF indicates that the value is unknown.</span></span> <span data-ttu-id="67bab-313">Diese Eigenschaft wird auf jedem Sicherungs Domänen Controller (BDC) in der Domäne separat verwaltet.</span><span class="sxs-lookup"><span data-stu-id="67bab-313">This property is maintained separately on each backup domain controller (BDC) in the domain.</span></span> <span data-ttu-id="67bab-314">Um einen exakten Wert zu erhalten, sollte nur der größte Wert aus allen BDCs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67bab-314">To get an accurate value, only the largest value from all BDCs should be used.</span></span>

<span data-ttu-id="67bab-315">Beispiel: 4</span><span class="sxs-lookup"><span data-stu-id="67bab-315">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="67bab-316">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="67bab-316">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-319">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ para")</span><span class="sxs-lookup"><span data-stu-id="67bab-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_parms")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-320">Leerraum, der für die Verwendung durch Anwendungen reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-320">Space set aside for use by applications.</span></span> <span data-ttu-id="67bab-321">Diese Zeichenfolge kann NULL sein, oder Sie kann eine beliebige Anzahl von Zeichen vor dem abschließenden NULL-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="67bab-321">This string can be null, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="67bab-322">Microsoft-Produkte verwenden dieses Mitglied zum Speichern von Benutzer Konfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="67bab-322">Microsoft products use this member to store user configuration information.</span></span> <span data-ttu-id="67bab-323">Ändern Sie diese Informationen nicht, da dieser Wert für eine Anwendung spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-323">Do not modify this information, because this value is specific to an application.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-324">**PasswordAge**</span><span class="sxs-lookup"><span data-stu-id="67bab-324">**PasswordAge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-325">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="67bab-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-327">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ Age")</span><span class="sxs-lookup"><span data-stu-id="67bab-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_password\_age")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-328">Die Zeitspanne, für die ein Kennwort wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-328">Length of time a password has been in effect.</span></span> <span data-ttu-id="67bab-329">Dieser Wert wird von der Anzahl der Sekunden gemessen, die seit der letzten Änderung des Kennworts verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="67bab-329">This value is measured from the number of seconds elapsed since the password was last changed.</span></span>

<span data-ttu-id="67bab-330">Beispiel: 00001201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="67bab-330">Example: 00001201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="67bab-331">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="67bab-331">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-332">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="67bab-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-334">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**Benutzer \_ modals \_ Info \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ Kennwort \_ Age")</span><span class="sxs-lookup"><span data-stu-id="67bab-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_MODALS\_INFO\_0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0)\|usrmod0\_max\_passwd\_age")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-335">Datum und Uhrzeit des Ablaufs des Kennworts.</span><span class="sxs-lookup"><span data-stu-id="67bab-335">Date and time the password expires.</span></span> <span data-ttu-id="67bab-336">Der Wert wird im folgenden Format festgelegt: YYYYMMDDHHMMSS. mmmmmm sutc</span><span class="sxs-lookup"><span data-stu-id="67bab-336">The value is set in this format: yyyymmddhhmmss.mmmmmm sutc</span></span>

<span data-ttu-id="67bab-337">Beispiel: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="67bab-337">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="67bab-338">**PrimaryGroupId**</span><span class="sxs-lookup"><span data-stu-id="67bab-338">**PrimaryGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-339">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-341">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Primary \_ Group \_ ID")</span><span class="sxs-lookup"><span data-stu-id="67bab-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_primary\_group\_id")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-342">Relativer Bezeichner (RID) der primären globalen Gruppe für diesen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="67bab-342">Relative identifier (RID) of the Primary Global Group for this user.</span></span> <span data-ttu-id="67bab-343">Der Bezeichner überprüft die primäre Gruppe, zu der das Profil des Benutzers gehört.</span><span class="sxs-lookup"><span data-stu-id="67bab-343">The identifier verifies the primary group to which the user's profile belongs.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-344">**Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="67bab-344">**Privileges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-345">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-345">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-347">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ PRIV")</span><span class="sxs-lookup"><span data-stu-id="67bab-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_priv")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-348">Ebene der Berechtigung, die der **usri3 \_ Name** -Eigenschaft zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-348">Level of privilege assigned to the **usri3\_name** property.</span></span>

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

<span data-ttu-id="67bab-349">**Gast** (0)</span><span class="sxs-lookup"><span data-stu-id="67bab-349">**Guest** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

<span data-ttu-id="67bab-350">**Benutzer** (1)</span><span class="sxs-lookup"><span data-stu-id="67bab-350">**User** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

<span data-ttu-id="67bab-351">**Administrator** (2)</span><span class="sxs-lookup"><span data-stu-id="67bab-351">**Administrator** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67bab-352">**Profil**</span><span class="sxs-lookup"><span data-stu-id="67bab-352">**Profile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-355">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ profile")</span><span class="sxs-lookup"><span data-stu-id="67bab-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_profile")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-356">Der Pfad zum Profil des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="67bab-356">Path to the user's profile.</span></span> <span data-ttu-id="67bab-357">Dieser Wert kann eine NULL-Zeichenfolge, ein lokaler absoluter Pfad oder ein UNC-Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="67bab-357">This value can be a null string, a local absolute path, or a UNC path.</span></span> <span data-ttu-id="67bab-358">Ein Benutzerprofil enthält Einstellungen, die für jeden Benutzer anpassbar sind, z. b. die Desktop Farben.</span><span class="sxs-lookup"><span data-stu-id="67bab-358">A user profile contains settings that are customizable for each user such as the desktop colors.</span></span>

<span data-ttu-id="67bab-359">Beispiel: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="67bab-359">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="67bab-360">**ScriptPath**</span><span class="sxs-lookup"><span data-stu-id="67bab-360">**ScriptPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-361">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-363">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Script \_ path")</span><span class="sxs-lookup"><span data-stu-id="67bab-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_script\_path")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-364">Verzeichnispfad zum Anmelde Skript des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="67bab-364">Directory path to the user's logon script.</span></span> <span data-ttu-id="67bab-365">Ein Anmelde Skript führt automatisch eine Reihe von Befehlen aus, wenn sich ein Benutzer bei einem System anmeldet.</span><span class="sxs-lookup"><span data-stu-id="67bab-365">A logon script automatically executes a set of commands each time a user logs on to a system.</span></span>

<span data-ttu-id="67bab-366">Beispiel: "C: \\ Win \\ Profiles \\ thomassteven"</span><span class="sxs-lookup"><span data-stu-id="67bab-366">Example: "C:\\win\\profiles\\ThomasSteven"</span></span>

</dd> <dt>

<span data-ttu-id="67bab-367">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="67bab-367">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-368">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-369">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-370">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="67bab-370">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67bab-371">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-371">Identifier by which the current object is known.</span></span>

<span data-ttu-id="67bab-372">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="67bab-372">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="67bab-373">**UnitsPerWeek**</span><span class="sxs-lookup"><span data-stu-id="67bab-373">**UnitsPerWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-374">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-376">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Units \_ per \_ Week")</span><span class="sxs-lookup"><span data-stu-id="67bab-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_units\_per\_week")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-377">Die Anzahl der Zeiteinheiten, in die die Woche aufgeteilt ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-377">Number of time units the week is divided into.</span></span> <span data-ttu-id="67bab-378">Sie wird mit der **LogonHours** -Eigenschaft verwendet, um den Benutzer Zugriff auf den Computer einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="67bab-378">It is used with the **LogonHours** property to limit user access to the computer.</span></span>

<span data-ttu-id="67bab-379">Beispiel: 168 (Stunden pro Woche)</span><span class="sxs-lookup"><span data-stu-id="67bab-379">Example: 168 (hours per week)</span></span>

</dd> <dt>

<span data-ttu-id="67bab-380">**UserComment**</span><span class="sxs-lookup"><span data-stu-id="67bab-380">**UserComment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-383">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ comment")</span><span class="sxs-lookup"><span data-stu-id="67bab-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_usr\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-384">Benutzerdefinierter Kommentar oder Beschreibung für dieses Profil.</span><span class="sxs-lookup"><span data-stu-id="67bab-384">User-defined comment or description for this profile.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-385">**UserId**</span><span class="sxs-lookup"><span data-stu-id="67bab-385">**UserId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-386">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bab-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-388">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ User \_ ID")</span><span class="sxs-lookup"><span data-stu-id="67bab-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_user\_id")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-389">Entfernen Sie den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="67bab-389">RID of the user.</span></span> <span data-ttu-id="67bab-390">Der Bezeichner überprüft, ob der Benutzer vorhanden und für diese Domäne eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="67bab-390">The identifier verifies that the user exists and is unique to this domain.</span></span>

</dd> <dt>

<span data-ttu-id="67bab-391">**UserType**</span><span class="sxs-lookup"><span data-stu-id="67bab-391">**UserType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-392">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-394">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags")</span><span class="sxs-lookup"><span data-stu-id="67bab-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-395">Der Kontotyp, für den der Benutzer über Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="67bab-395">Type of account to which the user has privileges.</span></span>

<span data-ttu-id="67bab-396">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="67bab-396">The values are:</span></span>

-   <span data-ttu-id="67bab-397">"Normales Konto"</span><span class="sxs-lookup"><span data-stu-id="67bab-397">"Normal Account"</span></span>
-   <span data-ttu-id="67bab-398">"Doppeltes Konto"</span><span class="sxs-lookup"><span data-stu-id="67bab-398">"Duplicate Account"</span></span>
-   <span data-ttu-id="67bab-399">"Arbeitsstations-Vertrauens Konto"</span><span class="sxs-lookup"><span data-stu-id="67bab-399">"Workstation Trust Account"</span></span>
-   <span data-ttu-id="67bab-400">"Server Vertrauensstellungs Konto"</span><span class="sxs-lookup"><span data-stu-id="67bab-400">"Server Trust Account"</span></span>
-   <span data-ttu-id="67bab-401">"Vertrauenswürdiges Domänen Konto"</span><span class="sxs-lookup"><span data-stu-id="67bab-401">"Interdomain Trust Account"</span></span>
-   <span data-ttu-id="67bab-402">Unbekannter</span><span class="sxs-lookup"><span data-stu-id="67bab-402">"Unknown"</span></span>

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="67bab-403">**Normales Konto** ("normales Konto")</span><span class="sxs-lookup"><span data-stu-id="67bab-403">**Normal Account** ("Normal Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="67bab-404">**Doppeltes Konto** ("doppeltes Konto")</span><span class="sxs-lookup"><span data-stu-id="67bab-404">**Duplicate Account** ("Duplicate Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="67bab-405">Arbeitsstations **Vertrauens Konto** ("Arbeitsstations-Vertrauensstellungs Konto")</span><span class="sxs-lookup"><span data-stu-id="67bab-405">**Workstation Trust Account** ("Workstation Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="67bab-406">**Server Vertrauensstellungs Konto** ("Server Vertrauensstellungs Konto")</span><span class="sxs-lookup"><span data-stu-id="67bab-406">**Server Trust Account** ("Server Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="67bab-407">**Domänen Vertrauensstellungs Konto** ("interdomäne-Vertrauensstellungs Konto")</span><span class="sxs-lookup"><span data-stu-id="67bab-407">**Interdomain Trust Account** ("Interdomain Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67bab-408">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="67bab-408">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67bab-409">**Arbeitsstationen**</span><span class="sxs-lookup"><span data-stu-id="67bab-409">**Workstations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67bab-410">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="67bab-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67bab-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="67bab-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67bab-412">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ Info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Workstations")</span><span class="sxs-lookup"><span data-stu-id="67bab-412">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_workstations")</span></span>
</dt> </dl>

<span data-ttu-id="67bab-413">Namen von Arbeitsstationen, von denen der Benutzer sich anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="67bab-413">Names of workstations from which the user can log on.</span></span> <span data-ttu-id="67bab-414">Es können bis zu acht Arbeitsstationen angegeben werden. die Namen müssen durch Kommas (,) getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="67bab-414">Up to eight workstations can be specified; the names must be separated by commas (,).</span></span> <span data-ttu-id="67bab-415">Eine NULL-Zeichenfolge weist keine Einschränkungen auf.</span><span class="sxs-lookup"><span data-stu-id="67bab-415">A null string indicates no restrictions.</span></span> <span data-ttu-id="67bab-416">Um Anmeldungen von allen Arbeitsstationen für dieses Konto zu deaktivieren, legen Sie die Eigenschaft "UF \_ accountdeaktiviert" in der **Flags** -Eigenschaft dieser Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="67bab-416">To disable logons from all workstations to this account, set the UF\_ACCOUNTDISABLE in the **Flags** property of this class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67bab-417">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67bab-417">Remarks</span></span>

<span data-ttu-id="67bab-418">Die **Win32- \_ networkloginprofile** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="67bab-418">The **Win32\_NetworkLoginProfile** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="67bab-419">Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="67bab-419">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="67bab-420">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="67bab-420">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

## <a name="examples"></a><span data-ttu-id="67bab-421">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67bab-421">Examples</span></span>

<span data-ttu-id="67bab-422">Das PowerShell-Beispiel " [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) " gibt Netzwerk Anmelde Informationen für alle Benutzer eines Computers zurück.</span><span class="sxs-lookup"><span data-stu-id="67bab-422">The [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) PowerShell sample returns network login information for all the users of a computer.</span></span>

<span data-ttu-id="67bab-423">Im folgenden VBScript-Beispiel werden Netzwerk Anmelde Informationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67bab-423">The following VBScript sample returns network login information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



## <a name="requirements"></a><span data-ttu-id="67bab-424">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67bab-424">Requirements</span></span>



| <span data-ttu-id="67bab-425">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67bab-425">Requirement</span></span> | <span data-ttu-id="67bab-426">Wert</span><span class="sxs-lookup"><span data-stu-id="67bab-426">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67bab-427">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67bab-427">Minimum supported client</span></span><br/> | <span data-ttu-id="67bab-428">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67bab-428">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67bab-429">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67bab-429">Minimum supported server</span></span><br/> | <span data-ttu-id="67bab-430">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67bab-430">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67bab-431">Namespace</span><span class="sxs-lookup"><span data-stu-id="67bab-431">Namespace</span></span><br/>                | <span data-ttu-id="67bab-432">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="67bab-432">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="67bab-433">MOF</span><span class="sxs-lookup"><span data-stu-id="67bab-433">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67bab-434"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="67bab-434"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="67bab-435">DLL</span><span class="sxs-lookup"><span data-stu-id="67bab-435">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67bab-436"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67bab-436"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67bab-437">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67bab-437">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67bab-438">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="67bab-438">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="67bab-439">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="67bab-439">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
