---
title: Identitäts Konstanten (appmodel. h)
description: Gibt die Länge der Zeichen folgen für die Identitäts Felder des Pakets an.
ms.assetid: C4F81822-B502-4360-AEA4-829F1AB926BF
topic_type:
- apiref
api_name:
- APPLICATION_USER_MODEL_ID_MAX_LENGTH
- APPLICATION_USER_MODEL_ID_MIN_LENGTH
- PACKAGE_ARCHITECTURE_MAX_LENGTH
- PACKAGE_ARCHITECTURE_MIN_LENGTH
- PACKAGE_FAMILY_NAME_MAX_LENGTH
- PACKAGE_FAMILY_NAME_MIN_LENGTH
- PACKAGE_FULL_NAME_MAX_LENGTH
- PACKAGE_FULL_NAME_MIN_LENGTH
- PACKAGE_NAME_MAX_LENGTH
- PACKAGE_NAME_MIN_LENGTH
- PACKAGE_PUBLISHERID_MAX_LENGTH
- PACKAGE_PUBLISHERID_MIN_LENGTH
- PACKAGE_PUBLISHER_MAX_LENGTH
- PACKAGE_PUBLISHER_MIN_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH
- PACKAGE_RESOURCEID_MAX_LENGTH
- PACKAGE_RESOURCEID_MIN_LENGTH
- PACKAGE_VERSION_MAX_LENGTH
- PACKAGE_VERSION_MIN_LENGTH
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681a0aef767afe92cdb93eee3849df8ed6a5f080
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339134"
---
# <a name="identity-constants"></a>Identitäts Konstanten

Gibt die Länge der Zeichen folgen für die Identitäts Felder des Pakets an. Die Länge wird in Zeichen gemessen und kann Leerzeichen für das NULL-Terminator enthalten.

> [!Note]  
> Konstanten in der Form: die Länge der **Anwendungs \_ Benutzer \_ Modell- \_ ID \_ \* \_** und die **\_ relative Anwendungs- \_ \_ ID \_ \* \_ des Pakets** enthalten Leerzeichen für ein NULL-Terminator, aber Konstanten in der Form: die **Paket \_ \* \_ Länge** enthalten keinen Platz für ein NULL-Terminator.

 



| Konstante/Wert                                                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**Anwendung \_ Benutzer \_ Modell- \_ ID \_ Maximale \_ Länge**</dt> <dt>130</dt> </dl>                  | Die maximale Länge der App-Benutzer Modell-ID. Für das NULL-Terminator ist ein Leerzeichen enthalten.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**Anwendung \_ Benutzer \_ Modell- \_ ID \_ Min. \_ Länge**</dt> <dt>21</dt> </dl>                   | Die minimale Länge der App-Benutzer Modell-ID. Für das NULL-Terminator ist ein Leerzeichen enthalten.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**Paket \_ \_Maximale \_ Länge der Architektur**</dt> <dt>7</dt> </dl>                                     | Die maximale Länge der Architektur. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**Paket \_ Architektur \_ minimale \_ Länge**</dt> <dt>3</dt> </dl>                                     | Die minimale Länge der Architektur. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**Paket \_ Familien \_ Name \_ Max. \_ Länge**</dt> <dt>64</dt> </dl>                                      | Die maximale Länge des Familiennamens. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**Paket \_ Familien \_ Name \_ Min. \_ Länge**</dt> <dt>17</dt> </dl>                                      | Die minimale Länge des Familiennamens. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**Paket \_ Vollständiger \_ Name der \_ maximalen \_ Länge**</dt> <dt>127</dt> </dl>                                           | Die maximale Länge des vollständigen Namens. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**Paket \_ Vollständiger \_ Name \_ Min. \_ Länge**</dt> <dt>30</dt> </dl>                                            | Die minimale Länge des vollständigen Namens. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**Paket \_ \_Maximale \_ Länge des Namens**</dt> <dt>50</dt> </dl>                                                            | Die maximale Länge des Namens. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**Paket \_ Name \_ minimale \_ Länge**</dt> <dt>3</dt> </dl>                                                             | Die minimale Länge des Namens. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**Paket \_ PublisherID, \_ Maximale \_ Länge**</dt> <dt>13</dt> </dl>                                       | Die maximale Länge der Herausgeber-ID. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**Paket \_ PublisherID \_ Min. \_ Länge**</dt> <dt>13</dt> </dl>                                       | Die Mindestlänge der Herausgeber-ID. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**Paket \_ \_Maximale Verleger \_ Länge**</dt> <dt>8192</dt> </dl>                                           | Die maximale Länge des Verlegers. Beispiel: CN =*Publisher*. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**Paket \_ Verleger \_ minimale \_ Länge**</dt> <dt>4</dt> </dl>                                              | Die minimale Länge des Verlegers. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**Paket \_ RELATIVE \_ Anwendungs- \_ ID, \_ Maximale \_ Länge**</dt> <dt>65</dt> </dl> | Die maximale Länge der relativen Anwendungs-ID des Pakets. Für das NULL-Terminator ist ein Leerzeichen enthalten.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**Paket \_ RELATIVE \_ Anwendungs- \_ ID \_ Min. \_ Länge**</dt> <dt>2</dt> </dl>  | Die minimale Länge der Paket relativen Anwendungs-ID. Für das NULL-Terminator ist ein Leerzeichen enthalten.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**Paket \_ Maximale ResourceId- \_ \_ Länge**</dt> <dt>30</dt> </dl>                                          | Die maximale Länge der Ressourcen-ID. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**Paket \_ ResourceId \_ Min. \_ Länge**</dt> <dt>0</dt> </dl>                                           | Die Mindestlänge der Ressourcen-ID. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**Paket \_ \_Maximale \_ Länge der Version**</dt> <dt>23</dt> </dl>                                                   | Die maximale Länge der Version. Beispielsweise *XXXXX*. *XXXXX*. *XXXXX*. *XXXXX*. Kein Leerzeichen für das NULL-Terminator enthalten.<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**Paket \_ \_Minimale \_ Länge der Version**</dt> <dt>7</dt> </dl>                                                    | Die Mindestlänge der Version. Beispiel: *x*. *x*. *x*. *x*. Es ist kein Leerzeichen für das NULL-Terminator enthalten.<br/>                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Appmodel. h</dt> </dl> |



 

 





