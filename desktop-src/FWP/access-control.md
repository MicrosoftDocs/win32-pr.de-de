---
title: Access Control (Windows-Filter Plattform)
description: In der Windows-Filter Plattform (WFP) implementiert der Dienst für die Basis Filter-Engine (BFE) das standardmäßige Windows-Zugriffs Steuerungsmodell, das auf Zugriffs Token und Sicherheits Beschreibungen basiert.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350988"
---
# <a name="access-control-windows-filtering-platform"></a>Access Control (Windows-Filter Plattform)

In der Windows-Filter Plattform (WFP) implementiert der Dienst für die Basis Filter-Engine (BFE) das standardmäßige [Windows-Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model) , das auf Zugriffs Token und Sicherheits Beschreibungen basiert.

## <a name="access-control-model"></a>Access Control Modell

Sicherheits Beschreibungen können beim Hinzufügen neuer WFP-Objekte, z. b. Filter und Unterebenen, angegeben werden. Sicherheits Deskriptoren werden mithilfe der WFP-Verwaltungsfunktionen " **swpm \* GetSecurityInfo0** " und " **\* SetSecurityInfo0**" verwaltet, wobei "* *\** _" für den Namen des WFP-Objekts steht. Diese Funktionen sind semantisch identisch mit den Funktionen Windows [_ *GetSecurityInfo* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) und [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

> [!Note]  
> Die **fwpm \* SetSecurityInfo0** -Funktionen können nicht innerhalb einer expliziten Transaktion aufgerufen werden.

 

> [!Note]  
> Die **fwpm \* SetSecurityInfo0** -Funktionen können nur innerhalb einer dynamischen Sitzung aufgerufen werden, wenn Sie zum Verwalten eines dynamischen Objekts verwendet werden, das innerhalb derselben Sitzung erstellt wurde.

 

Die Standard Sicherheits Beschreibung für die Filter-Engine (das Stamm-Engine-Objekt im folgenden Diagramm) lautet wie folgt.

-   Erteilen Sie der integrierten Gruppe "Administratoren" allgemeine Zugriffsrechte ( **Allgemein \_** verfügbar).
-   Erteilen von **generischen \_ Read** (GR) generic **\_ Write** ( **GW \_ )-** Zugriffsrechten für Netzwerk Konfigurations Operatoren.
-   Erteilen Sie den folgenden Dienst Sicherheits-IDs (SSIDs) **grgwgx** -Zugriffsrechte: mpssvc (Windows-Firewall), NAPAgent (Netzwerk Zugriffsschutz-Agent), policyagent (IPSec-Richtlinien-Agent), RPCSS (Remote Prozedur Aufrufe) und wdiservicehost (Diagnosedienst Host).
-   Gewähren Sie **fwpm \_ actrl \_ Open** und **fwpm \_ actrl \_** für jeden. (Hierbei handelt es sich um WFP-spezifische Zugriffsrechte, die in der folgenden Tabelle beschrieben werden.)

Die übrigen Standard Sicherheits Deskriptoren werden durch Vererbung abgeleitet.

Es gibt einige Zugriffs Überprüfungen, wie z. b. für die Funktion "Add0", "f", "f", "", "f", " **\* f** ", die Funktionsaufrufe von " **\***", **\*** Für diese Funktionen gibt es Containerobjekte für jeden Objekttyp. Bei den Standard Objekttypen (z. b. Anbietern, Legenden, Filtern) werden die vorhandenen Funktionen für die Funktion " **\* GetSecurityInfo0** " und " **\* SetSecurityInfo0** " überlastet, sodass ein NULL- **GUID** -Parameter den zugeordneten Container identifiziert. Für die anderen Objekttypen (z. b. Netzwerkereignisse und IPSec-Sicherheits Zuordnungen) gibt es explizite Funktionen zum Verwalten der Sicherheitsinformationen des Containers.

BFE unterstützt die automatische Vererbung von DACL-Zugriffs Steuerungs Einträgen (diskret Access Control List). BFE unterstützt keine SACL-ACEs (System Access Control List). -Objekte erben ACEs von Ihrem Container. Container erben ACEs von der Filter-Engine. Die weitergabepfade werden im folgenden Diagramm dargestellt.

![Diagramm, das die ACE-propagierungs Pfade anzeigt, beginnend mit "Engine".](images/access-control.jpg)

Für die Standard Objekttypen erzwingt BFE alle allgemeinen und standardmäßigen Zugriffsrechte. Außerdem definiert WFP die folgenden spezifischen Zugriffsrechte.



| WFP-Zugriffsrecht                                                                                                                        | BESCHREIBUNG                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**Hinzufügen von "f"- \_ actrl \_**<br/>                                       | Erforderlich zum Hinzufügen eines Objekts zu einem Container.<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**\_ \_ Link zum Hinzufügen von "f"-actrl \_**<br/>                       | Erforderlich, um eine Zuordnung zu einem Objekt zu erstellen. Wenn Sie z. b. einen Filter hinzufügen möchten, der auf eine Legende verweist, muss der Aufrufer über die Berechtigung Link hinzufügen \_ für die Legende verfügen.<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**f- \_ v-actrl \_ Begin \_ Read \_**<br/>    | Erforderlich, um eine explizite Lese Transaktion zu starten.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**f/a- \_ \_ \_ Schreibvorgänge starten \_**<br/> | Erforderlich, um eine explizite Schreib Transaktion zu starten.<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_kwpm-actrl- \_ Klassifizierung**<br/>                        | Erforderlich, um eine Klassifizierung mit einer benutzermodusebene durchzusetzen.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**WPM- \_ actrl-Aufzählung \_**<br/>                                    | Erforderlich, um die-Objekte in einem Container aufzuzählen. Der Enumerator gibt jedoch nur Objekte zurück, für die der Aufrufer über fwpm \_ actrl \_ Lesezugriff verfügt.<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**geöffnetes WPM- \_ actrl \_**<br/>                                    | Erforderlich, um eine Sitzung mit BFE zu öffnen.<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**\_Lesezugriff auf die Datei \_**<br/>                                    | Erforderlich, um die Eigenschaften eines Objekts zu lesen.<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**Lese Statistik für das awpm- \_ actrl \_ \_**<br/>                 | Erforderlich zum Lesen von Statistiken.<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**Konto für die \_ Anmeldung mit dem \_ Anmelde Namen**<br/>                     | Erforderlich zum Abonnieren von Benachrichtigungen. Abonnenten erhalten nur dann Benachrichtigungen für Objekte, auf die Sie über fwpm- \_ actrl- \_ Lesezugriff verfügen.<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**f- \_ \_ /Schreibzugriff**<br/>                                 | Erforderlich, um Engine-Optionen festzulegen.<br/>                                                                                                                               |



 

BFE überspringt alle Zugriffs Überprüfungen für Aufrufer im Kernel Modus.

Um zu verhindern, dass sich Administratoren selbst aus den BFE sperren, wird den Mitgliedern der integrierten Gruppe "Administratoren" immer die **fwpm-Zugriffs \_ \_ Berechtigung für** das Engine-Objekt erteilt. Daher kann ein Administrator mithilfe der folgenden Schritte wieder Zugriff erhalten.

-   Aktivieren Sie die Berechtigung zum **\_ Übernehmen des \_ Besitz Besitzes \_** .
-   [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)abrufen. Der Aufruf ist erfolgreich, da der Aufrufer ein Member integrierter Administratoren ist.
-   Übernimmt den Besitz des Engine-Objekts. Dies ist erfolgreich, da der Aufrufer über die Berechtigung zum Akzeptieren des **\_ \_ Besitz Besitzes \_** verfügt.
-   Aktualisieren Sie die DACL. Dies ist erfolgreich, weil der Besitzer immer über Schreibzugriff auf **\_ DAC** verfügt.

Da BFE seine eigene benutzerdefinierte Überwachung unterstützt, werden keine generischen Objekt Zugriffs Überwachungen generiert. Daher wird die SACL ignoriert.

## <a name="wfp-required-access-rights"></a>Erforderliche WFP-Zugriffsrechte

Die folgende Tabelle zeigt die Zugriffsrechte, die für die WFP-Funktionen erforderlich sind, um auf verschiedene Filter Platt Form Objekte zuzugreifen. Die **Funktionen von "f wpmfilter \* *_" werden als Beispiel für den Zugriff auf die Standardobjekte aufgeführt. Alle anderen Funktionen, die auf Standardobjekte zugreifen, folgen dem* Zugriffs Modell für \* die _** -voll Zugriffs Filter-Funktionen.



Funktion

Objekt geprüft

Erforderlicher Zugriff

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

Engine

**geöffnetes WPM- \_ actrl \_**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

Engine

**\_Lesezugriff auf die Datei \_**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

Engine

**f- \_ \_ /Schreibzugriff**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

Engine

**WPM- \_ actrl-Aufzählung \_**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

Engine

"F" **\_ actrl \_ Begin \_ Read \_ TXn**  &  **\_ BTRL \_ Begin \_ Write \_ TXn**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Container Anbieter<br/> Ebene<br/> Sub-Layer<br/> Legende<br/> Anbieter Kontext<br/>

**Link zum Hinzufügen von "f. \_ actrl \_ addfwpm \_ actrl" \_ \_**<br/> **\_ \_ Link zum Hinzufügen von "f"-actrl \_**<br/> **\_ \_ Link zum Hinzufügen von "f"-actrl \_**<br/> **\_ \_ Link zum Hinzufügen von "f"-actrl \_**<br/> **\_ \_ Link zum Hinzufügen von "f"-actrl \_**<br/>

[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

Filter

**DELETE**

[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

Filter

**\_Lesezugriff auf die Datei \_**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

Container Filter<br/>

**Lesevorgänge für die Konto- \_ actrl- \_ aufzuruf \_ \_**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

Container

**Konto für die \_ Anmeldung mit dem \_ Anmelde Namen**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

Container

**\_Lesezugriff auf die Datei \_**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

IPSec-SA-DB

**Lese Statistik für das awpm- \_ actrl \_ \_**

[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

IPSec-SA-DB

**Hinzufügen von "f"- \_ actrl \_**

[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

IPSec-SA-DB

**DELETE**

[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

IPSec-SA-DB

**\_Lesezugriff auf die Datei \_**

[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

IPSec-SA-DB

"F" **\_ actrl \_**-Aufzählungs-  &  **f- \_ \_ Lese** Vorgänge

[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

IKE-SA-DB

**Lese Statistik für das awpm- \_ actrl \_ \_**

[**IkeextSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

IKE-SA-DB

**DELETE**

[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

IKE-SA-DB

**\_Lesezugriff auf die Datei \_**

[**IkeextSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

IKE-SA-DB

"F" **\_ actrl \_**-Aufzählungs-  &  **f- \_ \_ Lese** Vorgänge

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

Container

**WPM- \_ actrl-Aufzählung \_**

[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

Keine weiteren Zugriffs Überprüfungen außerhalb der einzelnen Filter und Anbieter Kontexte



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Standard Zugriffsrechte**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Windows-Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Windows-Filterungs Plattform-Zugriffsrechte Bezeichner**](access-right-identifiers.md)
</dt> </dl>

 

