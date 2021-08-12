---
title: Identitätskonst constants (AppModel.h)
description: Gibt die Länge der Zeichenfolgen für die Identitätsfelder des Pakets an.
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
ms.openlocfilehash: 4590e62397ac069cb0fc9661f615288c2d8df36ba41304fff71e4ef0293f9f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552212"
---
# <a name="identity-constants"></a>Identitätskonst constants

Gibt die Länge der Zeichenfolgen für die Identitätsfelder des Pakets an. Die Länge wird in Zeichen gemessen und darf Platz für das NULL-Abschlusszeichen enthalten.

> [!Note]  
> Konstanten im Folgenden: **APPLICATION USER MODEL ID \_ \_ \_ \_ \* \_ LENGTH** und PACKAGE RELATIVE APPLICATION ID **\_ \_ \_ \_ \* \_ LENGTH** enthalten Speicherplatz für ein NULL-Abschlusszeichen, aber Konstanten im Folgenden: PACKAGE **\_ \* \_ LENGTH** enthalten keinen Platz für ein NULL-Abschlusszeichen.

 



| Konstante/Wert                                                                                                                                                                                                                                                                                                   | Beschreibung                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**ANWENDUNG \_ \_ \_ BENUTZERMODELL-ID \_ \_ MAX. LÄNGE**</dt> <dt>130</dt> </dl>                  | Die maximale Länge der Benutzermodell-ID der Anwendung. Für das NULL-Abschlusszeichen ist Speicherplatz enthalten.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**ANWENDUNG \_ \_ \_ BENUTZERMODELL-ID \_ MIN \_ LENGTH**</dt> <dt>21</dt> </dl>                   | Die minimale Länge der Benutzermodell-ID der Anwendung. Für das NULL-Abschlusszeichen ist Speicherplatz enthalten.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**PACKAGE \_ ARCHITEKTUR \_ \_ MAX. LÄNGE**</dt> <dt>7</dt> </dl>                                     | Die maximale Länge der Architektur. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**PACKAGE \_ ARCHITEKTUR: \_ \_ MINDESTLÄNGE**</dt> <dt>3</dt> </dl>                                     | Die Mindestlänge der Architektur. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**PACKAGE \_ FAMILY \_ NAME \_ MAX \_ LENGTH**</dt> <dt>64</dt> </dl>                                      | Die maximale Länge des Familiennamens. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**PACKAGE \_ FAMILY \_ NAME \_ MIN \_ LENGTH**</dt> <dt>17</dt> </dl>                                      | Die Mindestlänge des Familiennamens. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**PACKAGE \_ VOLLSTÄNDIGER \_ NAME \_ \_ MAX. LÄNGE**</dt> <dt>127</dt> </dl>                                           | Die maximale Länge des vollständigen Namens. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**PACKAGE \_ VOLLSTÄNDIGER \_ NAME \_ \_ MIN. LÄNGE**</dt> <dt>30</dt> </dl>                                            | Die Mindestlänge des vollständigen Namens. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**PACKAGE \_ NAME \_ MAX \_ LENGTH**</dt> <dt>50</dt> </dl>                                                            | Die maximale Länge des Namens. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**PACKAGE \_ NAME \_ MIN \_ LENGTH**</dt> <dt>3</dt> </dl>                                                             | Die Mindestlänge des Namens. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**PACKAGE \_ PUBLISHERID \_ MAX \_ LENGTH**</dt> <dt>13</dt> </dl>                                       | Die maximale Länge der Herausgeber-ID. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**PACKAGE \_ PUBLISHERID \_ MIN \_ LENGTH**</dt> <dt>13</dt> </dl>                                       | Die Mindestlänge der Herausgeber-ID. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**PACKAGE \_ PUBLISHER \_ MAX \_ LENGTH**</dt> <dt>8192</dt> </dl>                                           | Die maximale Länge des Herausgebers. Beispiel: CN=*Publisher*. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**PACKAGE \_ PUBLISHER \_ MIN \_ LENGTH**</dt> <dt>4</dt> </dl>                                              | Die Mindestlänge des Herausgebers. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**PACKAGE \_ RELATIVE \_ \_ ANWENDUNGS-ID \_ MAX \_ LENGTH**</dt> <dt>65</dt> </dl> | Die maximale Länge der relativen Anwendungs-ID des Pakets. Für das NULL-Abschlusszeichen ist Speicherplatz enthalten.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**PACKAGE \_ RELATIVE \_ \_ ANWENDUNGS-ID \_ MIN \_ LENGTH**</dt> <dt>2</dt> </dl>  | Die minimale Länge der relativen Anwendungs-ID des Pakets. Für das NULL-Abschlusszeichen ist Speicherplatz enthalten.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**PACKAGE \_ RESOURCEID \_ MAX \_ LENGTH**</dt> <dt>30</dt> </dl>                                          | Die maximale Länge der Ressourcen-ID. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**PACKAGE \_ RESOURCEID \_ MIN \_ LENGTH**</dt> <dt>0</dt> </dl>                                           | Die Mindestlänge der Ressourcen-ID. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**PACKAGE \_ VERSION \_ MAX \_ LENGTH**</dt> <dt>23</dt> </dl>                                                   | Die maximale Länge der Version. Beispiel: *xxxxx*. *xxxxx*. *xxxxx*. *xxxxx*. Kein Speicherplatz für das NULL-Abschlusszeichen enthalten/<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**PACKAGE \_ VERSION \_ MIN \_ LENGTH**</dt> <dt>7</dt> </dl>                                                    | Die Mindestlänge der Version. Beispiel: *x*. *x*. *x*. *x*. Für das NULL-Abschlusszeichen ist kein Leerzeichen enthalten.<br/>                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>AppModel.h</dt> </dl> |



 

 





