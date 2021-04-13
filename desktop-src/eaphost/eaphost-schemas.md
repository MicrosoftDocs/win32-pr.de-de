---
title: EAPHost und Legacy Schema
description: Beschreibt das EAPHost-Schema und das Legacy Schema zum Erstellen von XML-Konfigurationsdateien und Anmelde Informationen.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389640"
---
# <a name="eaphost-and-legacy-schema"></a><span data-ttu-id="a0381-103">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="a0381-103">EAPHost and Legacy Schema</span></span>

<span data-ttu-id="a0381-104">In diesem Thema werden das EAPHost-Schema und das Legacy Schema zum Erstellen von XML-Konfigurationsdateien und Anmelde Informationsdateien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a0381-104">This topic describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span>

## <a name="about-eaphost-and-legacy-schema"></a><span data-ttu-id="a0381-105">Informationen zu EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="a0381-105">About EAPHost and Legacy Schema</span></span>

<span data-ttu-id="a0381-106">Das Erstellen einer Konfigurations-XML-Datei beginnt mit dem [eaphostconfig](eaphostconfigschema-schema.md) -Schema. das Erstellen von Anmelde Informations-XML-Daten beginnt mit dem [eaphustusercredeneschema](eaphostusercredentialsschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="a0381-106">Creating configuration XML commences with the [eaphostconfig](eaphostconfigschema-schema.md) schema; creating credential XML commences with the [eaphostusercredentials](eaphostusercredentialsschema-schema.md) schema.</span></span>

<span data-ttu-id="a0381-107">Einige der systemeigenen und Legacy Schemas enthalten allgemeine Schema Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0381-107">Several of the native and legacy schema contain common schema elements.</span></span> <span data-ttu-id="a0381-108">Allgemeine Elemente, die in Methoden Konfiguration und Methoden Anmelde Informationen verwendet werden, werden in eine einzelne Schema Datei abstrahiert, die als "Common Schema" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="a0381-108">Common elements used in method configuration and method credentials are abstracted into a single schema file, referred to as the "common schema".</span></span>

<span data-ttu-id="a0381-109">Die Begriffe "Methoden Konfiguration" und "Verbindungs Eigenschaften" werden austauschbar verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0381-109">The terms "method configuration" and "connection properties" are used interchangeably.</span></span> <span data-ttu-id="a0381-110">Ebenso werden die Begriffe "Methoden Anmelde Informationen" und "Benutzereigenschaften" austauschbar verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0381-110">Likewise, the terms "method credentials" and "user properties" are also used interchangeably.</span></span>

## <a name="eaphost-schema"></a><span data-ttu-id="a0381-111">EAPHost-Schema</span><span class="sxs-lookup"><span data-stu-id="a0381-111">EAPHost Schema</span></span>



| <span data-ttu-id="a0381-112">Schema</span><span class="sxs-lookup"><span data-stu-id="a0381-112">Schema</span></span>                                                                        | <span data-ttu-id="a0381-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0381-113">Description</span></span>                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a0381-114">baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="a0381-114">baseeapmethodconfig</span></span>](baseeapmethodconfigschema-schema.md)                   | <span data-ttu-id="a0381-115">Enthält allgemeine Konfigurations Schema Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0381-115">Contains common configuration schema elements.</span></span>     |
| [<span data-ttu-id="a0381-116">baseeapmethoduseranmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="a0381-116">baseeapmethodusercredentials</span></span>](baseeapmethodusercredentialsschema-schema.md) | <span data-ttu-id="a0381-117">Enthält allgemeine Schema Elemente für Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="a0381-117">Contains common credential schema elements.</span></span>        |
| [<span data-ttu-id="a0381-118">eapcommon</span><span class="sxs-lookup"><span data-stu-id="a0381-118">eapcommon</span></span>](eapcommonschema-schema.md)                                       | <span data-ttu-id="a0381-119">Enthält die **eapmethodtype** -Element Definition.</span><span class="sxs-lookup"><span data-stu-id="a0381-119">Contains the **EapMethodType** element definition.</span></span> |
| [<span data-ttu-id="a0381-120">eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="a0381-120">eaphostconfig</span></span>](eaphostconfigschema-schema.md)                               | <span data-ttu-id="a0381-121">Enthält das EAPHost-Konfigurations Schema.</span><span class="sxs-lookup"><span data-stu-id="a0381-121">Contains EAPHost configuration schema.</span></span>             |
| [<span data-ttu-id="a0381-122">eaphustuseranmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="a0381-122">eaphostusercredentials</span></span>](eaphostusercredentialsschema-schema.md)             | <span data-ttu-id="a0381-123">Enthält das EAPHost-Anmelde Informations Schema.</span><span class="sxs-lookup"><span data-stu-id="a0381-123">Contains EAPHost credential schema.</span></span>                |



 

## <a name="legacy-schema"></a><span data-ttu-id="a0381-124">Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="a0381-124">Legacy Schema</span></span>



| <span data-ttu-id="a0381-125">Schema</span><span class="sxs-lookup"><span data-stu-id="a0381-125">Schema</span></span>                                                                            | <span data-ttu-id="a0381-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0381-126">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0381-127">baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-127">baseeapconnectionpropertiesv1</span></span>](baseeapconnectionpropertiesv1schema-schema.md)   | <span data-ttu-id="a0381-128">Enthält allgemeine Konfigurations Schema Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0381-128">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="a0381-129">baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-129">baseeapuserpropertiesv1</span></span>](baseeapuserpropertiesv1schema-schema.md)               | <span data-ttu-id="a0381-130">Enthält allgemeine Schema Elemente für Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="a0381-130">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="a0381-131">eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-131">eapconnectionpropertiesv1</span></span>](eapconnectionpropertiesv1schema-schema.md)           | <span data-ttu-id="a0381-132">Enthält allgemeine Konfigurations Schema Elemente.</span><span class="sxs-lookup"><span data-stu-id="a0381-132">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="a0381-133">eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-133">eapuserpropertiesv1</span></span>](eapuserpropertiesv1schema-schema.md)                       | <span data-ttu-id="a0381-134">Enthält allgemeine Schema Elemente für Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="a0381-134">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="a0381-135">eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-135">eaptlsconnectionpropertiesv1</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="a0381-136">Wird mit EAP-TLS verwendet, um die Konfigurationsdaten für die Authentifizierung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a0381-136">Is used with EAP-TLS to describe authentication configuration data.</span></span>                          |
| [<span data-ttu-id="a0381-137">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="a0381-137">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="a0381-138">Wird mit EAP-TLS verwendet, um die Konfigurationsdaten für die Authentifizierung ab Windows 7 zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a0381-138">Is used with EAP-TLS to describe authentication configuration data beginning with Windows 7.</span></span> |
| [<span data-ttu-id="a0381-139">eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-139">eaptlsuserpropertiesv1</span></span>](eaptlsuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="a0381-140">Wird mit EAP-TLS verwendet, um Authentifizierungs Anmelde Informationen und Anmelde Informations Optionen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a0381-140">Is used with EAP-TLS to describe authentication credentials and credential options.</span></span>          |
| [<span data-ttu-id="a0381-141">mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-141">mschapv2connectionpropertiesv1</span></span>](mschapv2connectionpropertiesv1schema-schema.md) | <span data-ttu-id="a0381-142">Wird mit MS-CHAPv2 verwendet, um die Authentifizierungs Konfigurationsdaten zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a0381-142">Is used with MS-CHAPv2 to describe authentication configuration data.</span></span>                        |
| [<span data-ttu-id="a0381-143">mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-143">mschapv2userpropertiesv1</span></span>](mschapv2userpropertiesv1schema-schema.md)             | <span data-ttu-id="a0381-144">Wird mit MS-CHAPv2 verwendet, um Authentifizierungs Anmelde Informationen und Anmelde Informations Optionen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a0381-144">Is used with MS-CHAPv2 to describe authentication credentials and credential options.</span></span>        |
| [<span data-ttu-id="a0381-145">mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-145">mspeapconnectionpropertiesv1</span></span>](mspeapconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="a0381-146">Wird mit PEAPv0 verwendet, um die Konfigurationsdaten für die Authentifizierung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a0381-146">Is used with PEAPv0 to describe authentication configuration data.</span></span>                           |
| [<span data-ttu-id="a0381-147">mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="a0381-147">mspeapconnectionpropertiesv2</span></span>](mspeapconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="a0381-148">Wird mit PEAPv0 verwendet, um die Konfigurationsdaten für die Authentifizierung ab Windows 7 zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a0381-148">Is used with PEAPv0 to describe authentication configuration data beginning with Windows 7.</span></span>  |
| [<span data-ttu-id="a0381-149">mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a0381-149">mspeapuserpropertiesv1</span></span>](mspeapuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="a0381-150">Wird mit PEAPv0 verwendet, um Authentifizierungs Anmelde Informationen und Anmelde Informations Optionen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a0381-150">Is used with PEAPv0 to describe authentication credentials and credential options.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="a0381-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a0381-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0381-152">Überprüfen von EAPHost-und Legacy-Schema Beispielen</span><span class="sxs-lookup"><span data-stu-id="a0381-152">Reviewing EAPHost and Legacy Schema Samples</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




