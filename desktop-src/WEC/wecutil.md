---
title: Wecutil.exe
description: Wecutil.exe ist ein Windows Event Collector-Hilfsprogramm, mit dem ein Administrator Abonnements für Ereignisse erstellen und verwalten kann, die von Remoteereignisquellen weitergeleitet werden, die das WS-Management unterstützen.
ms.assetid: 93ce25df-f829-43b9-96f2-7f2f291d100e
ms.tgt_platform: multiple
keywords:
- Wecutil.exe
topic_type:
- apiref
api_name:
- Wecutil.exe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e93e09bc4eed51448b686f0d18f00ecacaacd31d063c4905757d0185128ee64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750970"
---
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe ist ein Windows Event Collector-Hilfsprogramm, mit dem ein Administrator Abonnements für Ereignisse erstellen und verwalten kann, die von Remoteereignisquellen weitergeleitet werden, die das WS-Management unterstützen. Bei Befehlen, Optionen und Optionswerten wird die Groß-/Kleinschreibung für dieses Hilfsprogramm nicht beachtet.

Wenn Sie beim Ausführen von wecutil die Meldung "Der RPC-Server ist nicht verfügbar" oder "Die Schnittstelle ist unbekannt" erhalten, müssen Sie den Windows Event Collector-Dienst (wecsvc) starten. Geben Sie zum Starten von wecsvc an einer Eingabeaufforderung mit erhöhten Rechten **net start wecsvc ein.**

## <a name="list-existing-subscriptions"></a>Auflisten vorhandener Abonnements

Die folgende Syntax wird verwendet, um vorhandene Remoteereignisabonnements auflisten.

``` syntax
wecutil { es | enum-subscription }
```

Wenn Sie ein Skript verwenden, um die Namen der Abonnements aus der Ausgabe zu erhalten, müssen Sie die UTF-8-BOM-Zeichen in der ersten Zeile der Ausgabe umgehen. Das folgende Skript zeigt ein Beispiel dafür, wie Sie die BOM-Zeichen überspringen können.

``` syntax
setlocal enabledelayedexpansion

set bomskipped=
for /f %%i in ('wecutil es') do (
    set sub=%%i
    if not defined bomskipped (
        set sub=!sub:~3!
        set bomskipped=yes
    )
    echo !sub!
)
goto :eof

endlocal
```

## <a name="get-subscription-configuration"></a>Abonnementkonfiguration erhalten

Die folgende Syntax wird verwendet, um Konfigurationsdaten für Remoteereignisabonnements anzuzeigen.

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>Konfigurationsparameter erhalten

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ABONNEMENT-ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird im **SubscriptionId-Element** in der XML-Konfigurationsdatei angegeben, die zum Erstellen des Abonnements verwendet wird.

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:*VALUE***
</dt> <dd>

Ein -Wert, der die Ausgabe der Abonnementkonfigurationsdaten angibt. *VALUE* kann "XML" oder "Terse" sein, und der Standardwert ist "Terse". Wenn *VALUE* "XML" ist, wird die Ausgabe im XML-Format ausgegeben. Wenn *VALUE* "Terse" ist, wird die Ausgabe in Name-Wert-Paaren ausgegeben.

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***
</dt> <dd>

Ein -Wert, der angibt, ob die Ausgabe im Unicode-Format vorgibt. *VALUE* kann "true" oder "false" sein. Wenn *VALUE* auf "true" festgelegt ist, liegt die Ausgabe im Unicode-Format vor, und wenn *VALUE* "false" ist, liegt die Ausgabe nicht im Unicode-Format vor.

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>Get subscription runtime status (Abonnementlaufzeitstatus erhalten)

Die folgende Syntax wird verwendet, um den Abonnementlaufzeitstatus anzuzeigen.

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>Get Status Parameters

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ABONNEMENT-ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird im **SubscriptionId-Element** in der XML-Konfigurationsdatei angegeben, die zum Erstellen des Abonnements verwendet wird.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_EREIGNISQUELLE**
</dt> <dd>

Ein -Wert, der einen Computer identifiziert, der eine Ereignisquelle für ein Ereignisabonnement ist. Dieser Wert kann der vollqualifizierte Domänenname für den Computer, der NetBIOS-Name oder die IP-Adresse sein.

</dd> </dl>

## <a name="set-subscription-configuration-information"></a>Festlegen von Abonnementkonfigurationsinformationen

Die folgende Syntax wird zum Festlegen von Abonnementkonfigurationsdaten verwendet, indem Abonnementparameter über die Befehlszeile oder mithilfe einer XML-Konfigurationsdatei geändert werden.

``` syntax
wecutil { ss | set_subscription } SUBSCRIPTION_ID [/e:VALUE] 
[/esa:EVENT_SOURCE [/ese:VALUE] [/aes] [/res] [/un:USERNAME] [/up:PASSWORD]] 
[/d:DESCRIPTION] [/uri:URI] [/cm:CONFIGURATION_MODE] [/ex:DATE_TIME] 
[/q:QUERY] [/dia:DIALECT] [/tn:TRANSPORTNAME] [/tp:TRANSPORTPORT] [/dm:MODE] 
[/dmi:NUMBER] [/dmlt:MS] [/hi:MS] [/cf:FORMAT] [/l:LOCALE] [/ree:[VALUE]] 
[/lf:FILENAME] [/pn:PUBLISHER] [/hn:NAME] [/ct:TYPE] 
[/cun:USERNAME] [/cup:PASSWORD] 
[/ica:THUMBPRINTS] [/as:ALLOWED] [/ds:DENIED] [/adc:SDDL]

wecutil {ss | set_subscription } /c:CONGIG_FILE [/cun:USERNAME] 
[/cup:PASSWORD]
```

### <a name="remarks"></a>Hinweise

Wenn im Befehl **wecutil ss** ein falscher Benutzername oder ein falsches Kennwort angegeben ist, wird erst dann ein Fehler gemeldet, wenn Sie den Laufzeitstatus des Abonnements mithilfe des **Befehls wecutil gr** anzeigen.

## <a name="set-configuration-parameters"></a>Festlegen von Konfigurationsparametern

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ABONNEMENT-ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird im **SubscriptionId-Element** in der XML-Konfigurationsdatei angegeben, die zum Erstellen des Abonnements verwendet wird.

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG \_ FILE***
</dt> <dd>

Ein -Wert, der den Pfad zu der XML-Datei angibt, die Abonnementkonfigurationsinformationen enthält. Der Pfad kann absolut oder relativ zum aktuellen Verzeichnis sein. Dieser Parameter kann nur mit den optionalen Parametern /cus und /cup verwendet werden und ist mit allen anderen Parametern gegenseitig ausschließend.

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***
</dt> <dd>

Ein -Wert, der bestimmt, ob das Abonnement aktiviert oder deaktiviert werden soll. VALUE kann true oder false sein. Der Standardwert ist true, wodurch das Abonnement aktiviert wird.

> [!Note]  
> Wenn Sie ein vom Collector initiiertes Abonnement deaktivieren, wird die Ereignisquelle inaktiv und nicht deaktiviert. In einem vom Collector initiierten Abonnement können Sie eine Ereignisquelle unabhängig vom Abonnement deaktivieren.

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***
</dt> <dd>

Ein -Wert, der eine Beschreibung für das Ereignisabonnement angibt.

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE \_ TIME***
</dt> <dd>

Ein -Wert, der die Ablaufzeit des Abonnements angibt. *DATE \_ TIME* ist ein Wert, der im Standard-XML- oder ISO8601-Datums-/Uhrzeitformat angegeben ist: "yyyy-MM-ddThh:mm:ss .sss Z ", wobei "T" das Zeittrennzeichen und \[ \] \[ \] "Z" die UTC-Zeit angibt. Wenn DATE *\_ TIME* beispielsweise "2007-01-12T01:20:00" ist, ist die Abonnementablaufzeit der 12. Januar 2007, 01:20.

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***
</dt> <dd>

Ein -Wert, der den Typ der vom Abonnement verbrauchten Ereignisse angibt. Die Adresse des Ereignisquellencomputers zusammen mit dem URI (Uniform Resource Identifier) identifiziert die Quelle der Ereignisse eindeutig. Die URI-Zeichenfolge wird für alle Ereignisquellenadressen im Abonnement verwendet.

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *\_ KONFIGURATIONSMODUS***
</dt> <dd>

Ein -Wert, der den Konfigurationsmodus des Ereignisabonnements angibt. *KONFIGURATION \_ MODE* kann eine der folgenden Zeichenfolgen sein: "Normal", "Custom", "MinLatency" oder "MinBandwidth". Die [**EC SUBSCRIPTION CONFIGURATION \_ \_ \_ MODE-Enumeration**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) definiert die Konfigurationsmodi. Die Parameter /dm, /dmi, /hi und /dmlt können nur angegeben werden, wenn der Konfigurationsmodus auf Benutzerdefiniert festgelegt ist.

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***
</dt> <dd>

Ein -Wert, der die Abfragezeichenfolge für das Abonnement angibt. Das Format dieser Zeichenfolge kann für verschiedene URI-Werte unterschiedlich sein und gilt für alle Ereignisquellen im Abonnement.

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALEKT***
</dt> <dd>

Ein -Wert, der den von der Abfragezeichenfolge verwendeten Dialekt angibt.

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***
</dt> <dd>

Ein -Wert, der das Format der zurückgegebenen Ereignisse angibt. *FORMAT* kann "Events" oder "RenderedText" sein. Wenn der Wert "RenderedText" ist, werden die Ereignisse mit den lokalisierten Zeichenfolgen (z. B. Ereignisbeschreibungszeichenfolgen) zurückgegeben, die an die Ereignisse angefügt sind. Der Standardwert von *FORMAT* ist "RenderedText".

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *LOCALE***
</dt> <dd>

Ein -Wert, der das Locale für die Übermittlung der lokalisierten Zeichenfolgen im gerenderten Textformat angibt. *LOCALE* ist ein Sprachen-/Länderkulturbezeichner, z. B. "EN-us". Dieser Parameter ist nur gültig, wenn der Parameter /cf auf "RenderedText" festgelegt ist.

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree: \[ *VALUE*\]**
</dt> <dd>

Ein -Wert, der angibt, welche Ereignisse für das Abonnement übermittelt werden sollen. *VALUE* kann true oder false sein. Wenn *VALUE* true ist, werden alle vorhandenen Ereignisse aus den Abonnementereignisquellen gelesen. Wenn *VALUE* false ist, werden nur zukünftige (eintreffende) Ereignisse übermittelt. Der Standardwert ist TRUE, wenn /ree ohne Wert angegeben wird, und der Standardwert false, wenn /ree nicht angegeben ist.

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***
</dt> <dd>

Ein -Wert, der das lokale Ereignisprotokoll angibt, das zum Speichern von Ereignissen verwendet wird, die vom Ereignisabonnement empfangen wurden.

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***
</dt> <dd>

Ein -Wert, der den Namen des Ereignisherausgebers (Anbieters) angibt. Es muss ein Herausgeber sein, der das durch den /lf-Parameter angegebene Protokoll besitzt oder importiert.

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***
</dt> <dd>

Ein -Wert, der den Abonnementbereitstellungsmodus angibt. *MODE* kann entweder push oder pull sein. Diese Option ist nur gültig, wenn der Parameter /cm auf Benutzerdefiniert festgelegt ist.

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***
</dt> <dd>

Ein -Wert, der die maximale Anzahl von Elementen für die Batchbereitstellung im Ereignisabonnement angibt. Diese Option ist nur gültig, wenn der Parameter /cm auf Benutzerdefiniert festgelegt ist.

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***
</dt> <dd>

Ein -Wert, der die maximale Latenz angibt, die bei der Bereitstellung eines Ereignisbatches zulässig ist. MS ist die zulässige Anzahl von Millisekunden. Dieser Parameter ist nur gültig, wenn der Parameter /cm auf Benutzerdefiniert festgelegt ist.

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***
</dt> <dd>

Ein -Wert, der das Taktintervall für das Abonnement angibt. *MS* ist die Anzahl von Millisekunden, die im Intervall verwendet werden. Dieser Parameter ist nur gültig, wenn der Parameter /cm auf Benutzerdefiniert festgelegt ist.

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***
</dt> <dd>

Ein -Wert, der den Namen des Transports angibt, der zum Herstellen einer Verbindung mit dem Remoteereignisquellencomputer verwendet wird.

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/delegation: *EVENT \_ SOURCE***
</dt> <dd>

Ein -Wert, der die Adresse eines Ereignisquellencomputers angibt. *EVENT \_ SOURCE* ist eine Zeichenfolge, die einen Ereignisquellencomputer anhand des vollqualifizierten Domänennamens für den Computer, den NetBIOS-Namen oder die IP-Adresse identifiziert. Dieser Parameter kann mit den Parametern /ese, /aes, /res oder /un und /up verwendet werden.

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***
</dt> <dd>

Ein -Wert, der bestimmt, ob eine Ereignisquelle aktiviert oder deaktiviert werden soll. *VALUE* kann true oder false sein. Der Standardwert ist true, wodurch die Ereignisquelle aktiviert wird. Dieser Parameter wird nur verwendet, wenn der Parameter /parameters verwendet wird.

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/aes**
</dt> <dd>

Ein -Wert, der die ereignisquelle hinzufügt, die durch den Parameter /parameters angegeben wird, wenn die Ereignisquelle nicht bereits Teil des Ereignisabonnements ist. Wenn der durch den Parameter /ments angegebene Computer bereits Teil des Abonnements ist, wird ein Fehler angezeigt. Dieser Parameter ist nur zulässig, wenn der Parameter /delegation verwendet wird.

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/res**
</dt> <dd>

Ein -Wert, der die ereignisquelle entfernt, die durch den Parameter /parameters angegeben wird, wenn die Ereignisquelle bereits Teil des Ereignisabonnements ist. Wenn der durch den Parameter /ments angegebene Computer nicht Teil des Abonnements ist, wird ein Fehler angezeigt. Dieser Parameter ist nur zulässig, wenn der Parameter /delegation verwendet wird.

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *USERNAME***
</dt> <dd>

Ein -Wert, der den Benutzernamen angibt, der in den Anmeldeinformationen verwendet wird, um eine Verbindung mit der Ereignisquelle herzustellen, die im Parameter /parameters angegeben ist. Dieser Parameter ist nur zulässig, wenn der Parameter /delegation verwendet wird.

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***
</dt> <dd>

Ein -Wert, der das Kennwort für den im /un-Parameter angegebenen Benutzernamen angibt. Der Benutzername und die Kennwortanmeldeinformationen werden verwendet, um eine Verbindung mit der Ereignisquelle herzustellen, die im Parameter /parameters angegeben ist. Dieser Parameter ist nur zulässig, wenn der Parameter /un verwendet wird.

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***
</dt> <dd>

Ein -Wert, der die Portnummer angibt, die vom Transport beim Herstellen einer Verbindung mit einem Remoteereignisquellencomputer verwendet wird.

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***
</dt> <dd>

Ein -Wert, der den DNS-Namen des lokalen Computers angibt. Dieser Name wird von Remoteereignisquellen zum Pushen von Ereignissen verwendet und darf nur für Pushabonnements verwendet werden.

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***
</dt> <dd>

Ein -Wert, der den Anmeldeinformationstyp angibt, der für den Zugriff auf Remoteereignisquellen verwendet wird. *TYPE* kann "default", "negotiate", "digest", "basic" oder "localmachine" sein. Der Standardwert ist "default". Diese Werte werden in der [**EC \_ SUBSCRIPTION CREDENTIALS \_ \_ TYPE-Enumeration**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) definiert.

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***
</dt> <dd>

Ein -Wert, der die freigegebenen Benutzeranmeldeinformationen für Ereignisquellen ohne eigene Benutzeranmeldeinformationen fest legt.

> [!Note]  
> Wenn dieser Parameter mit der Option /c verwendet wird, werden die Benutzernamen- und Kennworteinstellungen für einzelne Ereignisquellen aus der Konfigurationsdatei ignoriert. Wenn Sie unterschiedliche Anmeldeinformationen für eine bestimmte Ereignisquelle verwenden möchten, können Sie diesen Wert überschreiben, indem Sie die Parameter /un und /up für eine bestimmte Ereignisquelle in der Befehlszeile eines anderen set-subscription-Befehls angeben.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***
</dt> <dd>

Ein -Wert, der das Benutzerkennwort für die freigegebenen Benutzeranmeldeinformationen fest legt. Wenn *PASSWORD* auf \* (Sternchen) festgelegt ist, wird das Kennwort aus der Konsole gelesen. Diese Option ist nur gültig, wenn der Parameter /cun angegeben wird.

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *FINGERABDRUCK***
</dt> <dd>

Ein -Wert, der die Liste der Ausstellerzertifikatfingerabdrucke in einer durch Komma getrennten Liste fest legt.

> [!Note]  
> Diese Option gilt nur für von der Quelle initiierte Abonnements.

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *ZULÄSSIG***
</dt> <dd>

Ein -Wert, der eine durch Komma getrennte Liste von Zeichenfolgen angibt, die die DNS-Namen von Nichtdomänencomputern angeben, die Abonnements initiieren dürfen. Die Namen können mithilfe von Platzhaltern angegeben werden, z. B. \* ".mydomain.com". Standardmäßig ist diese Liste leer.

> [!Note]  
> Diese Option gilt nur für von der Quelle initiierte Abonnements.

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***
</dt> <dd>

Ein -Wert, der eine durch Komma getrennte Liste von Zeichenfolgen angibt, die die DNS-Namen von Nichtdomänencomputern angeben, die keine Abonnements initiieren dürfen. Die Namen können mithilfe von Platzhaltern angegeben werden, z. B. \* ".mydomain.com". Standardmäßig ist diese Liste leer.

> [!Note]  
> Diese Option gilt nur für von der Quelle initiierte Abonnements.

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***
</dt> <dd>

Ein -Wert, der eine Zeichenfolge im SDDL-Format angibt, die angibt, welche Domänencomputer Abonnements initiieren dürfen oder nicht. Standardmäßig wird allen Domänencomputern das Initiieren von Abonnements ermöglicht.

> [!Note]  
> Diese Option gilt nur für von der Quelle initiierte Abonnements.

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>Erstellen eines neuen Abonnements

Die folgende Syntax wird verwendet, um ein Ereignisabonnement für Ereignisse auf einem Remotecomputer zu erstellen.

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>Hinweise

Wenn im Befehl **wecutil cs** ein falscher Benutzername oder ein falsches Kennwort angegeben ist, wird erst dann ein Fehler gemeldet, wenn Sie den Laufzeitstatus des Abonnements mithilfe des **Befehls wecutil gr** anzeigen.

## <a name="creation-parameters"></a>Erstellungsparameter

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**\_KONFIGURATIONSDATEI**
</dt> <dd>

Ein -Wert, der den Pfad zu der XML-Datei angibt, die Abonnementkonfigurationsinformationen enthält. Der Pfad kann absolut oder relativ zum aktuellen Verzeichnis sein.

Der folgende XML-Code ist ein Beispiel für eine Abonnementkonfigurationsdatei, die ein vom Collector initiiertes Abonnement erstellt, um Ereignisse aus dem Anwendungsereignisprotokoll eines Remotecomputers an das ForwardedEvents-Protokoll weiter zu senden.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleCISubscription</SubscriptionId>
    <SubscriptionType>CollectorInitiated</SubscriptionType>
    <Description>Collector Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>20</MaxItems>
            <MaxLatencyTime>60000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <HostName>thisMachine.myDomain.com</HostName>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2010-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>*</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>false</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <CredentialsType>Default</CredentialsType>

    <EventSources>
        <EventSource Enabled="true">
            <Address>mySource.myDomain.com</Address>
            <UserName>myUserName</UserName>
        </EventSource>
    </EventSources>
</Subscription>
```



Der folgende XML-Code ist ein Beispiel für eine Abonnementkonfigurationsdatei, die ein von der Quelle initiiertes Abonnement erstellt, um Ereignisse aus dem Anwendungsereignisprotokoll eines Remotecomputers an das ForwardedEvents-Protokoll weiter zu senden.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleSISubscription</SubscriptionId>
    <SubscriptionType>SourceInitiated</SubscriptionType>
    <Description>Source Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>1</MaxItems>
            <MaxLatencyTime>1000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2018-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>Event[System/EventID='999']</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>true</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
    <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
</Subscription>
```



> [!Note]  
> Wenn beim Erstellen eines von der Quelle initiierten Abonnements **AllowedSourceDomainComputers,** **AllowedSourceNonDomainComputers** / **IssuerCAList,** **AllowedSubjectList** und **DeniedSubjectList** leer sind, wird ein Standardwert für **AllowedSourceDomainComputers** bereitgestellt: "O:NSG:NSD:(A;; GA;;;D C)(A;; ALLGEMEINES;;; NS)". Diese SDDL-Standardeinstellung gewährt Mitgliedern der Domänengruppe Domänencomputer sowie der lokalen Netzwerkdienstgruppe (für die lokale Weitergeleitete) die Möglichkeit, Ereignisse für dieses Abonnement zu erstellen.

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***
</dt> <dd>

Ein -Wert, der die freigegebenen Benutzeranmeldeinformationen für Ereignisquellen ohne eigene Benutzeranmeldeinformationen fest legt. Dieser Wert gilt nur für vom Collector initiierte Abonnements.

> [!Note]  
> Wenn dieser Parameter angegeben wird, werden die Benutzernamen- und Kennworteinstellungen für einzelne Ereignisquellen aus der Konfigurationsdatei ignoriert. Wenn Sie unterschiedliche Anmeldeinformationen für eine bestimmte Ereignisquelle verwenden möchten, können Sie diesen Wert überschreiben, indem Sie die Parameter /un und /up für eine bestimmte Ereignisquelle in der Befehlszeile eines anderen set-subscription-Befehls angeben.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***
</dt> <dd>

Ein -Wert, der das Benutzerkennwort für die freigegebenen Benutzeranmeldeinformationen fest legt. Wenn *PASSWORD* auf " " (Sternchen) festgelegt ist, wird das \* Kennwort aus der Konsole gelesen. Diese Option ist nur gültig, wenn der Parameter /cun angegeben wird.

</dd> </dl>

## <a name="delete-a-subscription"></a>Löschen eines Abonnements

Die folgende Syntax wird verwendet, um ein Ereignisabonnement zu löschen.

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>Löschparameter

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ABONNEMENT-ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird im **SubscriptionId-Element** in der XML-Konfigurationsdatei angegeben, die zum Erstellen des Abonnements verwendet wird. Das in diesem Parameter identifizierte Abonnement wird gelöscht.

</dd> </dl>

## <a name="retry-a-subscription"></a>Wiederholen eines Abonnements

Die folgende Syntax wird verwendet, um ein inaktives Abonnement zu wiederholen, indem versucht wird, alle oder angegebene Ereignisquellen erneut zu aktivieren, indem eine Verbindung mit jeder Ereignisquelle hergestellt und eine Remoteabonnementanforderung an die Ereignisquelle sendet. Deaktivierte Ereignisquellen werden nicht wiederholt.

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>Wiederholungsparameter

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**\_ABONNEMENT-ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird im **SubscriptionId-Element** in der XML-Konfigurationsdatei angegeben, die zum Erstellen des Abonnements verwendet wird. Das in diesem Parameter identifizierte Abonnement wird wiederholt.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**\_EREIGNISQUELLE**
</dt> <dd>

Ein -Wert, der einen Computer identifiziert, der eine Ereignisquelle für ein Ereignisabonnement ist. Dieser Wert kann der vollqualifizierte Domänenname für den Computer, der NetBIOS-Name oder die IP-Adresse sein.

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>Konfigurieren des Windows Event Collector-Diensts

Die folgende Syntax wird verwendet, um den Windows Event Collector-Dienst zu konfigurieren, um sicherzustellen, dass Ereignisabonnements durch Computerneustarts erstellt und aufrechterhalten werden können. Dies schließt das folgende Verfahren ein:

**So konfigurieren Sie den Windows Event Collector-Dienst**

1.  Aktivieren Sie den ForwardedEvents-Kanal, wenn er deaktiviert ist.
2.  Verzögern Sie den Start des Windows Event Collector-Diensts.
3.  Starten Sie Windows Event Collector-Dienst, wenn er nicht ausgeführt wird.

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>Konfigurieren von Ereignissammlerparametern

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***
</dt> <dd>

Ein -Wert, der bestimmt, ob der Befehl quick-config zur Bestätigung aufgefordert wird. VALUE kann true oder false sein. Wenn VALUE true ist, fordert der Befehl zur Bestätigung auf. Der Standardwert ist „FALSE“.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

 





