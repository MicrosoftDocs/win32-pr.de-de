---
description: 'Die Programmierschnittstelle Webdienste auf Geräten definiert und verwendet die folgenden Strukturen:'
ms.assetid: daaa7d18-7af9-4f03-bbbd-378f4af79eec
title: Strukturen von Webdiensten auf Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4f963676dfdc8e7d931bb2c61fd1d661b30f544caf51d0d76e5bf79fc42612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920011"
---
# <a name="web-services-on-devices-structures"></a>Strukturen von Webdiensten auf Geräten

Die Programmierschnittstelle Webdienste auf Geräten definiert und verwendet die folgenden Strukturen:

-   [**REQUESTBODY \_ GetStatus**](/windows/win32/api/wsdtypes/ns-wsdtypes-requestbody_getstatus)
-   [**REQUESTBODY \_ Renew**](/windows/win32/api/wsdtypes/ns-wsdtypes-requestbody_renew)
-   [**REQUESTBODY \_ Subscribe**](/windows/win32/api/wsdtypes/ns-wsdtypes-requestbody_subscribe)
-   [**REQUESTBODY-Abonnement \_ kündigen**](/windows/win32/api/wsdtypes/ns-wsdtypes-requestbody_unsubscribe)
-   [**RESPONSEBODY \_ GetMetadata**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_getmetadata)
-   [**RESPONSEBODY \_ GetStatus**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_getstatus)
-   [**RESPONSEBODY \_ Renew**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_renew)
-   [**RESPONSEBODY \_ Subscribe**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_subscribe)
-   [**RESPONSEBODY \_ SubscriptionEnd**](/windows/win32/api/wsdtypes/ns-wsdtypes-responsebody_subscriptionend)
-   [**\_WSD-APP-SEQUENZ \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_app_sequence)
-   [**WSD \_ BYE**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_bye)
-   [**\_WSD-KONFIGURATIONSADRESSEN \_**](/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_addresses)
-   [**\_ \_ WSD-KONFIGURATIONS-PARAM**](/windows/desktop/api/wsdbase/ns-wsdbase-wsd_config_param)
-   [**WSD \_ DATETIME**](/windows/desktop/api/WsdXml/ns-wsdxml-wsd_datetime)
-   [**WSD-DAUER \_**](/windows/desktop/api/WsdXml/ns-wsdxml-wsd_duration)
-   [**\_WSD-ENDPUNKTREFERENZ \_**](/windows/desktop/api/Wsdtypes/ns-wsdtypes-wsd_endpoint_reference)
-   [**\_WSD-ENDPUNKTREFERENZLISTE \_ \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_endpoint_reference_list)
-   [**WSD-EREIGNIS \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_event)
-   [**\_WSD-EREIGNISBEREITSTELLUNGSMODUS \_ \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_delivery_mode)
-   [**PUSH IM \_ WSD-EREIGNISBEREITSTELLUNGSMODUS \_ \_ \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_delivery_mode_push)
-   [**\_WSD-EREIGNIS \_ LÄUFT AB**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_expires)
-   [**\_WSD-EREIGNISFILTER \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_filter)
-   [**\_WSD-EREIGNISFILTERAKTION \_ \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_eventing_filter_action)
-   [**\_WSD-HANDLERKONTEXT \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_handler_context)
-   [**\_WSD-HEADER \_ RELATESTO**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_header_relatesto)
-   [**WSD \_ HELLO**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_hello)
-   [**\_WSD-HOSTMETADATEN \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_host_metadata)
-   [**LOKALISIERTE \_ WSD-ZEICHENFOLGE \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_localized_string)
-   [**LOKALISIERTE \_ \_ WSD-ZEICHENFOLGENLISTE \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_localized_string_list)
-   [**\_WSD-METADATENABSCHNITT \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_metadata_section)
-   [**\_ \_ WSD-METADATENABSCHNITTSLISTE \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_metadata_section_list)
-   [**\_WSD-NAMENSLISTE \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_name_list)
-   [**WSD-VORGANG \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_operation)
-   [**\_WSD-PORTTYP \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_port_type)
-   [**WSD-TEST \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_probe)
-   [**WSD \_ PROBE \_ MATCH**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_probe_match)
-   [**WSD-TEST– \_ \_ \_ ÜBEREINSTIMMUNGSLISTE**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_probe_match_list)
-   [**WSD-TEST \_ \_ FINDET ÜBEREINSTIMMUNGEN**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_probe_matches)
-   [**\_WSD-REFERENZPARAMETER \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_reference_parameters)
-   [**\_WSD-REFERENZEIGENSCHAFTEN \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_reference_properties)
-   [**\_WSD-BEZIEHUNGSMETADATEN \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_relationship_metadata)
-   [**WSD \_ RESOLVE**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_resolve)
-   [**WSD \_ RESOLVE \_ MATCH**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_resolve_match)
-   [**\_WSD-AUFLÖSUNGS-ÜBEREINSTIMMUNGEN \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_resolve_matches)
-   [**\_WSD-BEREICHE**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_scopes)
-   [**\_WSD-SICHERHEITSZERTIFIKATÜBERPRÜFUNG \_ \_**](/windows/desktop/api/wsdbase/ns-wsdbase-wsd_security_cert_validation)
-   [**\_ \_ WSD-SICHERHEITSSIGNATURÜBERPRÜFUNG \_**](/windows/desktop/api/wsdbase/ns-wsdbase-wsd_security_signature_validation)
-   [**\_WSD-DIENSTMETADATEN \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_service_metadata)
-   [**\_WSD-DIENSTMETADATENLISTE \_ \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_service_metadata_list)
-   [**\_WSD-SOAP-FEHLER \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_fault)
-   [**\_ \_ WSD-SOAP-FEHLERCODE \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_fault_code)
-   [**\_ \_ WSD-SOAP-FEHLERGRUND \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_fault_reason)
-   [**\_ \_ WSD-SOAP-FEHLERUNTERCODE \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_fault_subcode)
-   [**\_WSD-SOAP-HEADER \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_header)
-   [**\_WSD-SOAP-NACHRICHT \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_soap_message)
-   [**SYNCHRONER \_ \_ WSD-ANTWORTKONTEXT \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_synchronous_response_context)
-   [**WSD \_ THIS \_ DEVICE \_ METADATA**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_this_device_metadata)
-   [**WSD \_ THIS \_ MODEL \_ METADATA**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_this_model_metadata)
-   [**UNBEKANNTE \_ \_ WSD-SUCHE**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_unknown_lookup)
-   [**\_WSD-URI-LISTE \_**](/windows/desktop/api/WsdTypes/ns-wsdtypes-wsd_uri_list)
-   [**WSDUdpRetransmitParams**](/windows/desktop/api/Wsdbase/ns-wsdbase-wsdudpretransmitparams)
-   [**WSDXML-ATTRIBUT \_**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_attribute)
-   [**WSDXML-ELEMENT \_**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_element)
-   [**WSDXML-ELEMENTLISTE \_ \_**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_element_list)
-   [**WSDXML-NAME \_**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_name)
-   [**WSDXML-NAMESPACE \_**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_namespace)
-   [**WSDXML-KNOTEN \_**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_node)
-   [**WSDXML-PRÄFIXZUORDNUNG \_ \_**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_prefix_mapping)
-   [**WSDXML-TEXT \_**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_text)
-   [**WSDXML-TYP \_**](/windows/desktop/api/WsdXmldom/ns-wsdxmldom-wsdxml_type)

 

 



