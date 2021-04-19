---
title: Extendeddisconnecationcode-Enumeration
description: Definiert erweiterte Informationen über den Grund für die Trennung der Verbindung.
ms.assetid: E73E73B4-6C6B-4270-A1BD-947FA6D7B31B
ms.tgt_platform: multiple
keywords:
- Extendeddisconnecationcode-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- ExtendedDisconnectReasonCode
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657d0faee03ca37b9a5a49b95b978a24b0c8955c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345511"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a><span data-ttu-id="41c20-104">Extendeddisconnecationcode-Enumeration</span><span class="sxs-lookup"><span data-stu-id="41c20-104">ExtendedDisconnectReasonCode enumeration</span></span>

<span data-ttu-id="41c20-105">Definiert erweiterte Informationen über den Grund für die Trennung der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="41c20-105">Defines extended information about the control's reason for disconnection.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c20-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="41c20-106">Syntax</span></span>


```C++
typedef enum _ExtendedDisconnectReasonCode { 
  exDiscReasonNoInfo                            = 0,
  exDiscReasonAPIInitiatedDisconnect            = 1,
  exDiscReasonAPIInitiatedLogoff                = 2,
  exDiscReasonServerIdleTimeout                 = 3,
  exDiscReasonServerLogonTimeout                = 4,
  exDiscReasonReplacedByOtherConnection         = 5,
  exDiscReasonOutOfMemory                       = 6,
  exDiscReasonServerDeniedConnection            = 7,
  exDiscReasonServerDeniedConnectionFips        = 8,
  exDiscReasonServerInsufficientPrivileges      = 9,
  exDiscReasonServerFreshCredsRequired          = 10,
  exDiscReasonRpcInitiatedDisconnectByUser      = 11,
  exDiscReasonLogoffByUser                      = 2,
  exDiscReasonLicenseInternal                   = 256,
  exDiscReasonLicenseNoLicenseServer            = 257,
  exDiscReasonLicenseNoLicense                  = 258,
  exDiscReasonLicenseErrClientMsg               = 259,
  exDiscReasonLicenseHwidDoesntMatchLicense     = 260,
  exDiscReasonLicenseErrClientLicense           = 261,
  exDiscReasonLicenseCantFinishProtocol         = 262,
  exDiscReasonLicenseClientEndedProtocol        = 263,
  exDiscReasonLicenseErrClientEncryption        = 264,
  exDiscReasonLicenseCantUpgradeLicense         = 265,
  exDiscReasonLicenseNoRemoteConnections        = 266,
  exDiscReasonLicenseCreatingLicStoreAccDenied  = 267,
  exDiscReasonRdpEncInvalidCredentials          = 768,
  exDiscReasonProtocolRangeStart                = 4096,
  exDiscReasonProtocolRangeEnd                  = 32767
} ExtendedDisconnectReasonCode;
```



## <a name="constants"></a><span data-ttu-id="41c20-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="41c20-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="41c20-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exdiscreasonnoinfo**</span><span class="sxs-lookup"><span data-stu-id="41c20-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-109">Es sind keine zusätzlichen Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41c20-109">No additional information is available.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exdiscreasonapiinitiateddisconnect**</span><span class="sxs-lookup"><span data-stu-id="41c20-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-111">Eine Anwendung hat die Trennung der Verbindung initiiert.</span><span class="sxs-lookup"><span data-stu-id="41c20-111">An application initiated the disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exdiscreasonapiinitiatedlogoff**</span><span class="sxs-lookup"><span data-stu-id="41c20-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-113">Eine Anwendung, die sich vom Client abgemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="41c20-113">An application logged off the client.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exdiscreasonserveridletimeout**</span><span class="sxs-lookup"><span data-stu-id="41c20-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-115">Der Server wurde vom Server getrennt, da der Client für einen Zeitraum im Leerlauf war, der länger als der festgelegte Timeout Zeitraum ist.</span><span class="sxs-lookup"><span data-stu-id="41c20-115">The server has disconnected the client because the client has been idle for a period of time longer than the designated time-out period.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exdiscreasonserverlogontimeout**</span><span class="sxs-lookup"><span data-stu-id="41c20-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-117">Der Server hat den Client getrennt, da der Client den für die Verbindung vorgesehenen Zeitraum überschritten hat.</span><span class="sxs-lookup"><span data-stu-id="41c20-117">The server has disconnected the client because the client has exceeded the period designated for connection.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exdiscreasonreplacedbyotherconnection**</span><span class="sxs-lookup"><span data-stu-id="41c20-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-119">Die Verbindung des Clients wurde durch eine andere Verbindung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="41c20-119">The client's connection was replaced by another connection.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exdiscreasonouto-Memory**</span><span class="sxs-lookup"><span data-stu-id="41c20-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-121">Es ist kein Arbeitsspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41c20-121">No memory is available.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exdiscreasonserverdeniedconnection**</span><span class="sxs-lookup"><span data-stu-id="41c20-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-123">Der Server hat die Verbindung verweigert.</span><span class="sxs-lookup"><span data-stu-id="41c20-123">The server denied the connection.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exdiscreasonserverdeniedconnectionfps**</span><span class="sxs-lookup"><span data-stu-id="41c20-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-125">Der Server hat die Verbindung aus Sicherheitsgründen verweigert.</span><span class="sxs-lookup"><span data-stu-id="41c20-125">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exdiscreasonserverinsuffizientprivileges**</span><span class="sxs-lookup"><span data-stu-id="41c20-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-127">Der Server hat die Verbindung aus Sicherheitsgründen verweigert.</span><span class="sxs-lookup"><span data-stu-id="41c20-127">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exdiscreasonserverfreshkredsrequired**</span><span class="sxs-lookup"><span data-stu-id="41c20-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-129">Es sind neue Anmelde Informationen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41c20-129">Fresh credentials are required.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exdiscreasonrpcinitiateddisconnectbyuser**</span><span class="sxs-lookup"><span data-stu-id="41c20-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-131">Die Benutzeraktivität hat die Verbindung initiiert.</span><span class="sxs-lookup"><span data-stu-id="41c20-131">User activity has initiated the disconnect.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exdiscreasonlogoffbyuser**</span><span class="sxs-lookup"><span data-stu-id="41c20-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-133">Der Benutzer hat sich angemeldet und trennt die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="41c20-133">The user logged off, disconnecting the session.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exdiscreasonlicenseinternal**</span><span class="sxs-lookup"><span data-stu-id="41c20-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-135">Interner Lizenzierungs Fehler.</span><span class="sxs-lookup"><span data-stu-id="41c20-135">Internal licensing error.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exdiscreasonlicensenolicenseserver**</span><span class="sxs-lookup"><span data-stu-id="41c20-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-137">Es war kein Lizenzserver verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41c20-137">No license server was available.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exdiscreasonlicensenolicense**</span><span class="sxs-lookup"><span data-stu-id="41c20-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-139">Es war keine gültige Software Lizenz verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41c20-139">No valid software license was available.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exdiscreasonlicenseerrclientmsg**</span><span class="sxs-lookup"><span data-stu-id="41c20-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-141">Der Remote Computer hat eine ungültige Lizenzierungs Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="41c20-141">The remote computer received a licensing message that was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exdiscreasonlicensehwiddoesntmatchlicense**</span><span class="sxs-lookup"><span data-stu-id="41c20-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-143">Die Hardware-ID stimmt nicht mit der Hardware-ID, die in der Software Lizenz angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="41c20-143">The hardware ID does not match the one designated on the software license.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exdiscreasonlicenseerrclientlicense**</span><span class="sxs-lookup"><span data-stu-id="41c20-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-145">Client Lizenz Fehler.</span><span class="sxs-lookup"><span data-stu-id="41c20-145">Client license error.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exdiscreasonlicensecantfinishprotocol**</span><span class="sxs-lookup"><span data-stu-id="41c20-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-147">Während des Lizenzierungs Protokolls sind Netzwerkprobleme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="41c20-147">Network problems occurred during the licensing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exdiscreasonlicenabclientendedprotocol**</span><span class="sxs-lookup"><span data-stu-id="41c20-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-149">Der Client hat das Lizenzierungs Protokoll vorzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="41c20-149">The client ended the licensing protocol prematurely.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exdiscreasonlicenseerrclientencryption**</span><span class="sxs-lookup"><span data-stu-id="41c20-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-151">Eine Lizenzierungs Nachricht wurde falsch verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="41c20-151">A licensing message was encrypted incorrectly.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exdiscreasonlicensecantupgradelicense**</span><span class="sxs-lookup"><span data-stu-id="41c20-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-153">Die Client Zugriffslizenz des lokalen Computers konnte nicht aktualisiert oder erneuert werden.</span><span class="sxs-lookup"><span data-stu-id="41c20-153">The local computer's client access license could not be upgraded or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exdiscreasonlicensenoremoteconnections**</span><span class="sxs-lookup"><span data-stu-id="41c20-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-155">Der Remote Computer ist nicht für die Annahme von Remote Verbindungen lizenziert.</span><span class="sxs-lookup"><span data-stu-id="41c20-155">The remote computer is not licensed to accept remote connections.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exdiscreasonlicensecreatinglicstoreaccdenied**</span><span class="sxs-lookup"><span data-stu-id="41c20-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-157">Beim Erstellen eines Registrierungsschlüssels für den Lizenz Speicher wurde ein Fehler vom Typ "Zugriff verweigert" empfangen.</span><span class="sxs-lookup"><span data-stu-id="41c20-157">An access denied error was received while creating a registry key for the license store.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exdiscreasonrdpcinvalidanmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="41c20-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-159">Ungültige Anmelde Informationen wurden gefunden.</span><span class="sxs-lookup"><span data-stu-id="41c20-159">Invalid credentials were encountered.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exdiscreasonprotocolrangestart**</span><span class="sxs-lookup"><span data-stu-id="41c20-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-161">Der Bereich interner Protokollfehler wird begonnen.</span><span class="sxs-lookup"><span data-stu-id="41c20-161">Beginning the range of internal protocol errors.</span></span> <span data-ttu-id="41c20-162">Weitere Informationen finden Sie im Ereignisprotokoll des Servers.</span><span class="sxs-lookup"><span data-stu-id="41c20-162">Check the server event log for additional details.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exdiscreasonprotocolrangeend**</span><span class="sxs-lookup"><span data-stu-id="41c20-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span></span>
</dt> <dd>

<span data-ttu-id="41c20-164">Der Bereich interner Protokollfehler wird beendet.</span><span class="sxs-lookup"><span data-stu-id="41c20-164">Ending the range of internal protocol errors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41c20-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41c20-165">Requirements</span></span>



| <span data-ttu-id="41c20-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41c20-166">Requirement</span></span> | <span data-ttu-id="41c20-167">Wert</span><span class="sxs-lookup"><span data-stu-id="41c20-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41c20-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41c20-168">Minimum supported client</span></span><br/> | <span data-ttu-id="41c20-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41c20-169">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="41c20-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41c20-170">Minimum supported server</span></span><br/> | <span data-ttu-id="41c20-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41c20-171">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="41c20-172">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="41c20-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="41c20-173"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-173"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c20-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41c20-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c20-175">**Extendeddisconnecverrat**</span><span class="sxs-lookup"><span data-stu-id="41c20-175">**ExtendedDisconnectReason**</span></span>](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





