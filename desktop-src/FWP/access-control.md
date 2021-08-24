---
title: Access Control (Windows Filterplattform)
description: In Windows Filterplattform (WFP) implementiert der BFE-Dienst (Base Filtering Engine) das Standardmodell Windows Zugriffssteuerung basierend auf Zugriffstoken und Sicherheitsbeschreibungen.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad8d1cc292358b156a8853a8a141426fda638d64474d1413747e2ebdb59d7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901095"
---
# <a name="access-control-windows-filtering-platform"></a>Access Control (Windows Filterplattform)

In Windows Filterplattform (WFP) implementiert der BFE-Dienst (Base Filtering Engine) das [Standardmodell Windows Zugriffssteuerung](/windows/desktop/SecAuthZ/access-control-model) basierend auf Zugriffstoken und Sicherheitsbeschreibungen.

## <a name="access-control-model"></a>Access Control-Modell

Sicherheitsbeschreibungen können beim Hinzufügen neuer WFP-Objekte wie Filter und Unterebenen angegeben werden. Sicherheitsbeschreibungen werden mit den WFP-Verwaltungsfunktionen **Fwpm \* GetSecurityInfo0** und **Fwpm \* SetSecurityInfo0** verwaltet, wobei * *\** _ für den Namen des WFP-Objekts steht. Diese Funktionen sind semantisch identisch mit den Funktionen Windows [_ *GetSecurityInfo* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) und [**SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

> [!Note]  
> Die **\* Fwpm-Funktionen SetSecurityInfo0** können nicht innerhalb einer expliziten Transaktion aufgerufen werden.

 

> [!Note]  
> Die **Fwpm \* SetSecurityInfo0-Funktionen** können nur innerhalb einer dynamischen Sitzung aufgerufen werden, wenn sie zum Verwalten eines dynamischen Objekts verwendet werden, das innerhalb derselben Sitzung erstellt wurde.

 

Die Standardsicherheitsbeschreibung für die Filter-Engine (das Stamm-Engine-Objekt im diagramm unten) lautet wie folgt.

-   Gewähren Sie der integrierten Administratorgruppe allgemeine Zugriffsrechte (GENERIC **\_ ALL,** GA).
-   Gewähren Sie DEN Netzwerkkonfigurationsoperatoren GENERIC **\_ READ** (GR) **GENERIC \_ WRITE** (GW) **GENERIC \_ EXECUTE** (GX).
-   Erteilen Sie **GRGWGX-Zugriffsrechte** für die folgenden Dienstsicherheits-IDs (SSIDs): MpsSvc (Windows Firewall), NapAgent (Network Access Protection Agent), PolicyAgent (IPsec Policy Agent), RpcSs (Remote Procedure Call) und WdiServiceHost (Diagnostic Service Host).
-   Gewähren Sie **FWPM \_ ACTRL \_ OPEN** und **FWPM \_ ACTRL \_ CLASSIFY** für alle Benutzer. (Dies sind WFP-spezifische Zugriffsrechte, die in der folgenden Tabelle beschrieben werden.)

Die verbleibenden Standardsicherheitsbeschreibungen werden durch Vererbung abgeleitet.

Es gibt einige Zugriffsüberprüfungen, z. B. für Funktionsaufrufe von **Fwpm \* Add0,** **Fwpm \* CreateEnumHandle0** und **Fwpm \* SubscribeChanges0,** die auf der Ebene einzelner Objekte nicht durchgeführt werden können. Für diese Funktionen gibt es Containerobjekte für jeden Objekttyp. Für die Standardobjekttypen (z. B. Anbieter, Aufrufe, Filter) werden die vorhandenen **Funktionen Fwpm \* GetSecurityInfo0** und **Fwpm \* SetSecurityInfo0** überladen, sodass ein **NULL-GUID-Parameter** den zugeordneten Container identifiziert. Für die anderen Objekttypen (z. B. Netzwerkereignisse und IPsec-Sicherheitszuordnungen) gibt es explizite Funktionen zum Verwalten der Sicherheitsinformationen des Containers.

BFE unterstützt die automatische Vererbung von DACL-Zugriffssteuerungseinträgen (Discretionary Access Control List). BFE unterstützt keine SACL-ACEs (System Access Control List). Objekte erben ACEs von ihrem Container. Container erben ACEs von der Filter-Engine. Die Weitergabepfade sind im folgenden Diagramm dargestellt.

![Diagramm, das die ACE-Weitergabepfade zeigt, beginnend mit "Engine".](images/access-control.jpg)

Für die Standardobjekttypen erzwingt BFE alle generischen und Standardzugriffsrechte. Darüber hinaus definiert WFP die folgenden spezifischen Zugriffsrechte.



| WFP-Zugriffsrecht                                                                                                                        | BESCHREIBUNG                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ ADD**<br/>                                       | Erforderlich, um einem Container ein Objekt hinzuzufügen.<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ LINK HINZUFÜGEN \_**<br/>                       | Erforderlich, um eine Zuordnung zu einem Objekt zu erstellen. Um beispielsweise einen Filter hinzuzufügen, der auf eine Aufrufliste verweist, muss der Aufrufer über ADD \_ LINK-Zugriff auf die -Aufrufliste verfügen.<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN**<br/>    | Erforderlich, um eine explizite Lesetransaktion zu starten.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN**<br/> | Erforderlich, um eine explizite Schreibtransaktion zu starten.<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ CLASSIFY**<br/>                        | Erforderlich, um eine Klassifizierung für eine Benutzermodusebene zu erstellen.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ \_ ACTRL-ENUMERATION**<br/>                                    | Erforderlich, um die Objekte in einem Container aufzuzählen. Der Enumerator gibt jedoch nur Objekte zurück, auf die der Aufrufer über FWPM \_ ACTRL \_ READ-Zugriff verfügt.<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ OPEN**<br/>                                    | Erforderlich, um eine Sitzung mit BFE zu öffnen.<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**<br/>                                    | Erforderlich, um die Eigenschaften eines Objekts zu lesen.<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ READ \_ STATS**<br/>                 | Zum Lesen von Statistiken erforderlich.<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ SUBSCRIBE**<br/>                     | Erforderlich, um Benachrichtigungen zu abonnieren. Abonnenten erhalten nur Benachrichtigungen für Objekte, auf die sie über FWPM \_ ACTRL \_ READ-Zugriff verfügen.<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ WRITE**<br/>                                 | Erforderlich, um Engine-Optionen festzulegen.<br/>                                                                                                                               |



 

BFE überspringt alle Zugriffsüberprüfungen für Aufrufer im Kernelmodus.

Um zu verhindern, dass Administratoren sich selbst von BFE sperren, wird Mitgliedern der integrierten Administratorengruppe immer **FWPM \_ ACTRL \_ OPEN** für das Engine-Objekt gewährt. Daher kann ein Administrator den Zugriff mithilfe der folgenden Schritte wiedererlangen.

-   Aktivieren Sie die **SE \_ TAKE OWNERSHIP \_ \_ NAME-Berechtigung.**
-   Rufen Sie [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)auf. Der Aufruf ist erfolgreich, da der Aufrufer Mitglied der integrierten Administratoren ist.
-   Übernehmen Sie den Besitz des Engine-Objekts. Dies ist erfolgreich, da der Aufrufer über die **SE \_ TAKE OWNERSHIP \_ \_ NAME-Berechtigung** verfügt.
-   Aktualisieren Sie die DACL. Dies ist erfolgreich, da der Besitzer immer über **\_ SCHREIB-DAC-Zugriff** verfügt.

Da BFE seine eigene benutzerdefinierte Überwachung unterstützt, werden keine generischen Objektzugriffsüberwachungen generiert. Daher wird die SACL ignoriert.

## <a name="wfp-required-access-rights"></a>Erforderliche WFP-Zugriffsrechte

Die folgende Tabelle zeigt die Zugriffsrechte, die für die WFP-Funktionen erforderlich sind, um auf verschiedene Filterplattformobjekte zuzugreifen. Die **FwpmFilter \* *_-Funktionen werden als Beispiel für den Zugriff auf die Standardobjekte aufgeführt. Alle anderen Funktionen, die auf Standardobjekte zugreifen, folgen dem* Zugriffsmodell _FwpmFilter-Funktionen. \***



Funktion

Objekt überprüft

Erforderlicher Zugriff

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

Engine

**FWPM \_ ACTRL \_ OPEN**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

Engine

**FWPM \_ ACTRL \_ READ**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

Engine

**FWPM \_ ACTRL \_ WRITE**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

Engine

**FWPM \_ \_ ACTRL-ENUMERATION**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

Engine

**FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN**  &  **FWPM \_ ACTRL BEGIN WRITE \_ \_ \_ TXN**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Containeranbieter<br/> Ebene<br/> Sub-Layer<br/> Legende<br/> Anbieterkontext<br/>

**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ LINK HINZUFÜGEN \_**<br/> **FWPM \_ ACTRL \_ LINK HINZUFÜGEN \_**<br/> **FWPM \_ ACTRL \_ LINK HINZUFÜGEN \_**<br/> **FWPM \_ ACTRL \_ LINK HINZUFÜGEN \_**<br/> **FWPM \_ ACTRL \_ LINK HINZUFÜGEN \_**<br/>

[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

Filtern

**DELETE**

[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

Filtern

**FWPM \_ ACTRL \_ READ**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

Containerfilter<br/>

**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ READ**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

Container

**FWPM \_ ACTRL \_ SUBSCRIBE**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

Container

**FWPM \_ ACTRL \_ READ**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

IPsec SA DB

**FWPM \_ ACTRL \_ READ \_ STATS**

[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

IPsec SA DB

**FWPM \_ ACTRL \_ ADD**

[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

IPsec SA DB

**DELETE**

[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

IPsec SA DB

**FWPM \_ ACTRL \_ READ**

[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

IPsec SA DB

**FWPM \_ ACTRL \_ ENUM**  &  **FWPM \_ ACTRL \_ READ**

[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

IKE SA DB

**FWPM \_ ACTRL \_ READ \_ STATS**

[**IkeextSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

IKE SA DB

**DELETE**

[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

IKE SA DB

**FWPM \_ ACTRL \_ READ**

[**IkeextSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

IKE SA DB

**FWPM \_ ACTRL \_ ENUM**  &  **FWPM \_ ACTRL \_ READ**

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

Container

**\_ \_ FWPM-ACTRL-ENUM**

[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

Keine zusätzlichen Zugriffsüberprüfungen über diejenigen hinaus für die einzelnen Filter und Anbieterkontexte



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Standardzugriffsrechte**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Windows des Zugriffssteuerungsmodells](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Windows Filtern von Bezeichnern für Plattformzugriffsrechte**](access-right-identifiers.md)
</dt> </dl>

 

