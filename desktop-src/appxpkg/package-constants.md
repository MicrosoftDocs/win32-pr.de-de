---
title: Paketkonst constants (AppModel.h)
description: Gibt an, wie Pakete verarbeitet werden sollen.
ms.assetid: 72E565C3-6CFD-47E3-8BAC-17D6E86B99DA
topic_type:
- apiref
api_name:
- PACKAGE_APPLICATIONS_MAX_COUNT
- PACKAGE_APPLICATIONS_MIN_COUNT
- PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES
- PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES
- PACKAGE_FILTER_ALL_LOADED
- PACKAGE_FILTER_BUNDLE
- PACKAGE_FILTER_DIRECT
- PACKAGE_FILTER_HEAD
- PACKAGE_FILTER_OPTIONAL
- PACKAGE_FILTER_RESOURCE
- PACKAGE_GRAPH_MAX_SIZE
- PACKAGE_GRAPH_MIN_SIZE
- PACKAGE_INFORMATION_BASIC
- PACKAGE_INFORMATION_FULL
- PACKAGE_MAX_DEPENDENCIES
- PACKAGE_MIN_DEPENDENCIES
- PACKAGE_PROPERTY_BUNDLE
- PACKAGE_PROPERTY_DEVELOPMENT_MODE
- PACKAGE_PROPERTY_FRAMEWORK
- PACKAGE_PROPERTY_OPTIONAL
- PACKAGE_PROPERTY_RESOURCE
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2b79d624940bfebb68ec2becc9cf3015d8405f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483186"
---
# <a name="package-constants"></a>Paketkonst constants

Gibt an, wie Pakete verarbeitet werden sollen.




| Konstante/Wert | BESCHREIBUNG | 
|----------------|-------------|
| <span id="PACKAGE_APPLICATIONS_MAX_COUNT"></span><span id="package_applications_max_count"></span><dl><dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt><dt>100</dt></dl> | Die maximale Anzahl von Apps in einem Paket.<br /> | 
| <span id="PACKAGE_APPLICATIONS_MIN_COUNT"></span><span id="package_applications_min_count"></span><dl><dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt><dt>0</dt></dl> | Die Mindestanzahl von Apps in einem Paket.<br /> | 
| <span id="PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES"></span><span id="package_family_max_resource_packages"></span><dl><dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt><dt>512</dt></dl> | Die maximale Anzahl von Ressourcenpaketen, die ein Paket enthalten kann.<br /> | 
| <span id="PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES"></span><span id="package_family_min_resource_packages"></span><dl><dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt><dt>0</dt></dl> | Die Mindestanzahl von Ressourcenpaketen, die ein Paket enthalten kann.<br /> | 
| <span id="PACKAGE_FILTER_ALL_LOADED"></span><span id="package_filter_all_loaded"></span><dl><dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt><dt>0x00000000</dt></dl> | Verarbeiten Sie alle Pakete im Abhängigkeitsdiagramm.<br /> Dies entspricht <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.<br /><blockquote>[!Note]<br /><strong>PACKAGE_FILTER_ALL_LOADED</strong> kann geändert werden oder für Releases nach der Windows 8.1. Verwenden Sie stattdessen <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.</blockquote><br /> | 
| <span id="PACKAGE_FILTER_BUNDLE"></span><span id="package_filter_bundle"></span><dl><dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt><dt>0x00000080</dt></dl> | Verarbeiten von Paketpaketen im Paketdiagramm.<br /> | 
| <span id="PACKAGE_FILTER_DIRECT"></span><span id="package_filter_direct"></span><dl><dt><strong>PACKAGE_FILTER_DIRECT</strong></dt><dt>0x00000020</dt></dl> | Verarbeiten Sie die direkt abhängigen Pakete des Hauptpakets (erstes Paket) im Abhängigkeitsdiagramm.<br /> | 
| <span id="PACKAGE_FILTER_HEAD"></span><span id="package_filter_head"></span><dl><dt><strong>PACKAGE_FILTER_HEAD</strong></dt><dt>0x00000010</dt></dl> | Verarbeiten Sie das erste Paket im Abhängigkeitsdiagramm.<br /> | 
| <span id="PACKAGE_FILTER_OPTIONAL"></span><span id="package_filter_optional"></span><dl><dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt><dt>0x00020000</dt></dl> | Verarbeiten von Paketpaketen im Paketdiagramm.<br /> | 
| <span id="PACKAGE_FILTER_RESOURCE"></span><span id="package_filter_resource"></span><dl><dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt><dt>0x00000040</dt></dl> | Verarbeiten von Ressourcenpaketen im Paketdiagramm.<br /> | 
| <span id="PACKAGE_GRAPH_MAX_SIZE"></span><span id="package_graph_max_size"></span><dl><dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt><dt>(1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES)</dt></dl> | Die maximale Größe eines Paketdiagramms.<br /> | 
| <span id="PACKAGE_GRAPH_MIN_SIZE"></span><span id="package_graph_min_size"></span><dl><dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt><dt>1</dt></dl> | Die Mindestgröße eines Paketdiagramms.<br /> | 
| <span id="PACKAGE_INFORMATION_BASIC"></span><span id="package_information_basic"></span><dl><dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt><dt>0x00000000</dt></dl> | Rufen Sie grundlegende Informationen ab.<br /> | 
| <span id="PACKAGE_INFORMATION_FULL"></span><span id="package_information_full"></span><dl><dt><strong>PACKAGE_INFORMATION_FULL</strong></dt><dt>0x00000100</dt></dl> | Rufen Sie vollständige Informationen ab.<br /> | 
| <span id="PACKAGE_MAX_DEPENDENCIES"></span><span id="package_max_dependencies"></span><dl><dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt><dt>128</dt></dl> | Die maximale Anzahl von Paketen, von der ein Paket abhängt.<br /> | 
| <span id="PACKAGE_MIN_DEPENDENCIES"></span><span id="package_min_dependencies"></span><dl><dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt><dt>0</dt></dl> | Die Mindestanzahl von Paketen, von der ein Paket abhängt.<br /> | 
| <span id="PACKAGE_PROPERTY_BUNDLE"></span><span id="package_property_bundle"></span><dl><dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt><dt>0x00000004</dt></dl> | Das Paket ist ein Paketpaket.<br /> | 
| <span id="PACKAGE_PROPERTY_DEVELOPMENT_MODE"></span><span id="package_property_development_mode"></span><dl><dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt><dt>0x00010000</dt></dl> | Das Paket wurde mit der <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>DeploymentOptions-Enumeration</strong></a> registriert.<br /> | 
| <span id="PACKAGE_PROPERTY_FRAMEWORK"></span><span id="package_property_framework"></span><dl><dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt><dt>0x00000001</dt></dl> | Das Paket ist ein Framework.<br /> | 
| <span id="PACKAGE_PROPERTY_OPTIONAL"></span><span id="package_property_optional"></span><dl><dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt><dt>0x00000008</dt></dl> | Das Paket ist ein optionales Paket.<br /> | 
| <span id="PACKAGE_PROPERTY_RESOURCE"></span><span id="package_property_resource"></span><dl><dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt><dt>0x00000002</dt></dl> | Das Paket ist ein Ressourcenpaket.<br /> | 




## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>AppModel.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetCurrentPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)
</dt> <dt>

[**GetPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)
</dt> <dt>

[**PackageIdFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)
</dt> </dl>

 

