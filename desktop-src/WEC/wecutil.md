---
title: Wecutil.exe
description: Wecutil.exe ist ein Windows-Ereignis Sammler-Hilfsprogramm, mit dem Administratoren Abonnements für Ereignisse erstellen und verwalten können, die von Remote Ereignis Quellen weitergeleitet werden, die das WS-Management-Protokoll unterstützen.
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
ms.openlocfilehash: aaf6f74007b56cff85c28c4106fd4345c5627d4e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353979"
---
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe ist ein Windows-Ereignis Sammler-Hilfsprogramm, mit dem Administratoren Abonnements für Ereignisse erstellen und verwalten können, die von Remote Ereignis Quellen weitergeleitet werden, die das WS-Management-Protokoll unterstützen. Bei Befehlen, Optionen und Options Werten wird die Groß-/Kleinschreibung für dieses Hilfsprogramm nicht beachtet.

Wenn Sie eine Meldung erhalten, die besagt, dass der RPC-Server nicht verfügbar ist oder die Schnittstelle unbekannt ist, müssen Sie den Windows-Ereignis Sammlungs Dienst (Wecsvc) starten, wenn Sie versuchen, wecutil auszuführen. Um Wecsvc zu starten, geben Sie an einer Eingabeaufforderung mit erhöhten Rechten **net Start Wecsvc** ein.

## <a name="list-existing-subscriptions"></a>Auflisten vorhandener Abonnements

Die folgende Syntax wird verwendet, um vorhandene Remote Ereignis Abonnements aufzulisten.

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

## <a name="get-subscription-configuration"></a>Abonnement Konfiguration erhalten

Die folgende Syntax wird verwendet, um Konfigurationsdaten für Remote Ereignis Abonnements anzuzeigen.

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>Konfigurationsparameter erhalten

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben.

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f: * Wert***
</dt> <dd>

Ein-Wert, der die Ausgabe der Abonnement Konfigurationsdaten angibt. Der Wert kann "XML" oder "Terse" lauten, der Standard *Wert* ist "Terse". Wenn *value* "XML" ist, wird die Ausgabe im XML-Format gedruckt. Wenn *value* "Terse" ist, wird die Ausgabe in Name-Wert-Paaren ausgegeben.

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *Wert***
</dt> <dd>

Ein-Wert, der angibt, ob die Ausgabe im Unicode-Format vorliegt. Der *Wert* kann "true" oder "false" lauten. Wenn *value den Wert* "true" hat, erfolgt die Ausgabe im Unicode-Format, und wenn *value den Wert* "false" hat, erfolgt die Ausgabe nicht im Unicode-Format.

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>Abonnement Lauf Zeit Status erhalten

Die folgende Syntax wird verwendet, um den Abonnement Lauf Zeit Status anzuzeigen.

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>Status Parameter erhalten

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**Ereignis \_ Quelle**
</dt> <dd>

Ein-Wert, der einen Computer identifiziert, bei dem es sich um eine Ereignis Quelle für ein Ereignis Abonnement handelt. Bei diesem Wert kann es sich um den voll qualifizierten Domänen Namen für den Computer, den NetBIOS-Namen oder die IP-Adresse handeln.

</dd> </dl>

## <a name="set-subscription-configuration-information"></a>Festlegen von Informationen zur Abonnement Konfiguration

Die folgende Syntax wird verwendet, um die Abonnement Konfigurationsdaten festzulegen, indem Sie die Abonnement Parameter von der Befehlszeile aus ändern oder eine XML-Konfigurationsdatei verwenden.

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

### <a name="remarks"></a>Bemerkungen

Wenn im Befehl " **wecutil SS** " ein falscher Benutzername oder ein falscher Kennwort angegeben ist, wird kein Fehler gemeldet, bis Sie den Lauf Zeit Status des Abonnements mit dem Befehl " **wecutil GR** " anzeigen.

## <a name="set-configuration-parameters"></a>Festlegen von Konfigurationsparametern

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben.

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *Konfigurations \_ Datei***
</dt> <dd>

Ein-Wert, der den Pfad zur XML-Datei angibt, die Informationen zur Abonnement Konfiguration enthält. Der Pfad kann absolut oder relativ zum aktuellen Verzeichnis sein. Dieser Parameter kann nur mit den optionalen Parametern/CUS und/Cup verwendet werden und schließt sich gegenseitig mit allen anderen Parametern aus.

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *Wert***
</dt> <dd>

Ein-Wert, der bestimmt, ob das Abonnement aktiviert oder deaktiviert werden soll. Der Wert kann "true" oder "false" sein. Der Standardwert ist "true", wodurch das Abonnement aktiviert wird.

> [!Note]  
> Wenn Sie ein vom Collector initiiertes Abonnement deaktivieren, wird die Ereignis Quelle nicht deaktiviert, sondern inaktiv. In einem vom Collector initiierten Abonnement können Sie eine Ereignis Quelle deaktivieren, die unabhängig vom Abonnement ist.

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Beschreibung***
</dt> <dd>

Ein-Wert, der eine Beschreibung für das Ereignis Abonnement angibt.

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/Ex: *Datum/ \_ Uhrzeit***
</dt> <dd>

Ein-Wert, der die Ablaufzeit des Abonnements angibt. *Datum \_ Time* ist ein Wert, der in Standard-XML-oder ISO8601-Datums-/Uhrzeitformat angegeben ist: "yyyy-mm-ddThh: mm: SS \[ . sss \] \[ Z \] ", wobei "T" das Zeit Trennzeichen und "Z" die UTC-Zeit angibt. Wenn z. b. *Datum/ \_ Uhrzeit* "2007-01-12t01:20:00" ist, ist die Ablaufzeit des Abonnements der 12. Januar 2007, 01:20.

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/URI: *URI***
</dt> <dd>

Ein-Wert, der den Typ der Ereignisse angibt, die vom Abonnement genutzt werden. Die Adresse des Ereignis Quell Computers zusammen mit dem URI (Uniform Resource Identifier) identifiziert die Quelle der Ereignisse eindeutig. Die URI-Zeichenfolge wird für alle Ereignis Quelladressen im Abonnement verwendet.

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *Konfigurations \_ Modus***
</dt> <dd>

Ein-Wert, der den Konfigurations Modus des Ereignis Abonnements angibt. *Konfiguration \_ Der Modus* kann eine der folgenden Zeichen folgen sein: "Normal", "Custom", "minlatency" oder "minbandwidth". Die [**\_ \_ Konfigurations \_ Modus**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) -Enumeration des EC-Abonnements definiert die Konfigurations Modi. Die Parameter/DM,/DMI,/Hi und/dmlt können nur angegeben werden, wenn der Konfigurations Modus auf Custom festgelegt ist.

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *Abfrage***
</dt> <dd>

Ein-Wert, der die Abfrage Zeichenfolge für das Abonnement angibt. Das Format dieser Zeichenfolge kann für unterschiedliche URI-Werte unterschiedlich sein und gilt für alle Ereignis Quellen im Abonnement.

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/Dia: *Dialekt***
</dt> <dd>

Ein-Wert, der den von der Abfrage Zeichenfolge verwendeten Dialekt angibt.

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF: *Format***
</dt> <dd>

Ein-Wert, der das Format der zurückgegebenen Ereignisse angibt. Das *Format* kann "Events" oder "renderedtext" lauten. Wenn der Wert "renderedtext" ist, werden die Ereignisse mit den lokalisierten Zeichen folgen (z. b. Ereignis Beschreibungs Zeichenfolgen) zurückgegeben, die den Ereignissen zugeordnet sind. Der Standardwert von *Format* ist "renderedtext".

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *Gebiets* Schema**
</dt> <dd>

Ein-Wert, der das Gebiets Schema für die Übermittlung der lokalisierten Zeichen folgen im gerenderten Textformat angibt. *Locale* ist ein sprach-/Länder Kultur Bezeichner, z. b. "en-US". Dieser Parameter ist nur gültig, wenn der/CF-Parameter auf "renderedtext" festgelegt ist.

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/Ree: \[ *Wert*\]**
</dt> <dd>

Ein-Wert, der angibt, welche Ereignisse für das Abonnement übermittelt werden sollen. Der *Wert* kann "true" oder "false" sein. Wenn *value den Wert* true hat, werden alle vorhandenen Ereignisse aus den Abonnement Ereignis Quellen gelesen. Wenn der *Wert* false ist, werden nur zukünftige (eingehende) Ereignisse übermittelt. Der Standardwert ist true, wenn/Ree ohne einen-Wert angegeben wird, und der Standardwert ist false, wenn/Ree nicht angegeben wird.

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF: *Dateiname***
</dt> <dd>

Ein-Wert, der das lokale Ereignisprotokoll angibt, das zum Speichern der vom Ereignis Abonnement empfangenen Ereignisse verwendet wird.

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN: *Publisher***
</dt> <dd>

Ein-Wert, der den Namen des Ereignis Verlegers (Anbieter) angibt. Dabei muss es sich um einen Verleger handeln, der das durch den/LF-Parameter angegebene Protokoll besitzt oder importiert.

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM: *Modus***
</dt> <dd>

Ein-Wert, der den abonnementzustellungs Modus angibt. Der *Modus* kann Push oder Pull lauten. Diese Option ist nur gültig, wenn der/cm-Parameter auf Custom festgelegt ist.

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI: *Zahl***
</dt> <dd>

Ein-Wert, der die maximale Anzahl von Elementen für die Batch Übermittlung im Ereignis Abonnement angibt. Diese Option ist nur gültig, wenn der/cm-Parameter auf Custom festgelegt ist.

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***
</dt> <dd>

Ein-Wert, der die maximale Latenz angibt, die für die Bereitstellung eines Batch von Ereignissen zulässig ist. MS ist die zulässige Anzahl von Millisekunden. Dieser Parameter ist nur gültig, wenn der/cm-Parameter auf Custom festgelegt ist.

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/Hi: *MS***
</dt> <dd>

Ein-Wert, der das Takt Intervall für das Abonnement angibt. *MS* ist die Anzahl der Millisekunden, die im Intervall verwendet werden. Dieser Parameter ist nur gültig, wenn der/cm-Parameter auf Custom festgelegt ist.

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *TransportName***
</dt> <dd>

Ein-Wert, der den Namen des Transports angibt, der zum Herstellen der Verbindung mit dem Remote-Ereignis Quellcomputer verwendet wird.

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ESA: *Ereignis \_ Quelle***
</dt> <dd>

Ein-Wert, der die Adresse eines Ereignis Quell Computers angibt. *Ereignis \_ Quelle* ist eine Zeichenfolge, die einen Ereignis Quellcomputer mit dem voll qualifizierten Domänen Namen für den Computer, den NetBIOS-Namen oder die IP-Adresse identifiziert. Dieser Parameter kann mit den Parametern/ESE,/AES,/res oder/UN und/up verwendet werden.

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ESE: *Wert***
</dt> <dd>

Ein Wert, der bestimmt, ob eine Ereignis Quelle aktiviert oder deaktiviert werden soll. Der *Wert* kann "true" oder "false" sein. Der Standardwert ist "true", wodurch die Ereignis Quelle aktiviert wird. Dieser Parameter wird nur verwendet, wenn der/ESA-Parameter verwendet wird.

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/aes**
</dt> <dd>

Ein-Wert, der die vom/ESA-Parameter angegebene Ereignis Quelle hinzufügt, wenn die Ereignis Quelle nicht bereits Teil des Ereignis Abonnements ist. Wenn der durch den/ESA-Parameter angegebene Computer bereits Teil des Abonnements ist, wird ein Fehler angezeigt. Dieser Parameter ist nur zulässig, wenn der/ESA-Parameter verwendet wird.

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/res**
</dt> <dd>

Ein-Wert, der die vom/ESA-Parameter angegebene Ereignis Quelle entfernt, wenn die Ereignis Quelle bereits Teil des Ereignis Abonnements ist. Wenn der durch den/ESA-Parameter angegebene Computer nicht Teil des Abonnements ist, wird ein Fehler angezeigt. Dieser Parameter ist nur zulässig, wenn der/ESA-Parameter verwendet wird.

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/UN: *Benutzername***
</dt> <dd>

Ein-Wert, der den Benutzernamen angibt, der in den Anmelde Informationen zum Herstellen einer Verbindung mit der im/ESA-Parameter angegebenen Ereignis Quelle verwendet wird. Dieser Parameter ist nur zulässig, wenn der/ESA-Parameter verwendet wird.

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *Kennwort***
</dt> <dd>

Ein-Wert, der das Kennwort für den Benutzernamen angibt, der im/UN-Parameter angegeben ist. Die Anmelde Informationen für Benutzername und Kennwort werden verwendet, um eine Verbindung mit der im/ESA-Parameter angegebenen Ereignis Quelle herzustellen. Dieser Parameter ist nur zulässig, wenn der/UN-Parameter verwendet wird.

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *transportport***
</dt> <dd>

Ein-Wert, der die Portnummer angibt, die vom Transport beim Herstellen einer Verbindung mit einem Remote-Ereignis Quellcomputer verwendet wird.

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN: *Name***
</dt> <dd>

Ein-Wert, der den DNS-Namen des lokalen Computers angibt. Dieser Name wird von Remote Ereignis Quellen verwendet, um Ereignisse per Push zurückzusetzen, und er muss nur für Pushabonnements verwendet werden.

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT: *Typ***
</dt> <dd>

Ein-Wert, der den Anmelde Informationstyp angibt, der für den Zugriff auf Remote Ereignis Quellen verwendet wird. *Type* kann "Default", "Aushandlungs", "Digest", "Basic" oder "LocalMachine" lauten. Der Standardwert ist "Default". Diese Werte werden in der [**\_ \_ \_ Type**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) -Enumeration der Anmelde Informationen des EC-Abonnements definiert.

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/Cun: *Benutzername***
</dt> <dd>

Ein-Wert, der die Anmelde Informationen für den freigegebenen Benutzer festlegt, die für Ereignis Quellen verwendet werden, die keine eigenen Anmelde Informationen besitzen.

> [!Note]  
> Wenn dieser Parameter mit der/c-Option verwendet wird, werden die Benutzernamen-und Kenn Wort Einstellungen für einzelne Ereignis Quellen aus der Konfigurationsdatei ignoriert. Wenn Sie andere Anmelde Informationen für eine bestimmte Ereignis Quelle verwenden möchten, können Sie diesen Wert überschreiben, indem Sie den/UN-Parameter und den/up-Parameter für eine bestimmte Ereignis Quelle in der Befehlszeile eines anderen Set-Abonnement-Befehls angeben.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *Kennwort***
</dt> <dd>

Ein-Wert, der das Benutzer Kennwort für die freigegebenen Benutzer Anmelde Informationen festlegt. Wenn *Password* auf \* (Sternchen) festgelegt ist, wird das Kennwort aus der Konsole gelesen. Diese Option ist nur gültig, wenn der/Cun-Parameter angegeben wird.

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA: Finger *Abdrücke***
</dt> <dd>

Ein-Wert, der die Liste der Fingerabdrücke für Aussteller Zertifikate in einer durch Trennzeichen getrennten Liste festlegt.

> [!Note]  
> Diese Option ist nur für Quellen initiierte Abonnements spezifisch.

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *zulässig***
</dt> <dd>

Ein Wert, der eine durch Trennzeichen getrennte Liste von Zeichen folgen festlegt, die die DNS-Namen von nicht-Domänen Computern angeben, die Abonnements initiieren dürfen. Die Namen können mithilfe von Platzhaltern angegeben werden, z \* . b. ". mydomain.com". Standardmäßig ist diese Liste leer.

> [!Note]  
> Diese Option ist nur für Quellen initiierte Abonnements spezifisch.

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS: *verweigert***
</dt> <dd>

Ein Wert, der eine durch Trennzeichen getrennte Liste von Zeichen folgen festlegt, die die DNS-Namen von nicht-Domänen Computern angeben, die keine Abonnements initiieren dürfen. Die Namen können mithilfe von Platzhaltern angegeben werden, z \* . b. ". mydomain.com". Standardmäßig ist diese Liste leer.

> [!Note]  
> Diese Option ist nur für Quellen initiierte Abonnements spezifisch.

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC: *SDDL***
</dt> <dd>

Ein Wert, der eine Zeichenfolge im SDDL-Format festlegt, die angibt, welche Domänen Computer zum Initiieren von Abonnements zulässig sind oder nicht. Standardmäßig wird allen Domänen Computern das Initiieren von Abonnements gestattet.

> [!Note]  
> Diese Option ist nur für Quellen initiierte Abonnements spezifisch.

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>Erstellen eines neuen Abonnements

Die folgende Syntax wird verwendet, um ein Ereignis Abonnement für Ereignisse auf einem Remote Computer zu erstellen.

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>Bemerkungen

Wenn im Befehl " **wecutil CS** " ein falscher Benutzername oder ein falscher Kennwort angegeben wird, wird kein Fehler gemeldet, bis Sie den Lauf Zeit Status des Abonnements mit dem Befehl " **wecutil GR** " anzeigen.

## <a name="creation-parameters"></a>Erstellungs Parameter

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**Konfigurations \_ Datei**
</dt> <dd>

Ein-Wert, der den Pfad zur XML-Datei angibt, die Informationen zur Abonnement Konfiguration enthält. Der Pfad kann absolut oder relativ zum aktuellen Verzeichnis sein.

Der folgende XML-Code ist ein Beispiel für eine Abonnement Konfigurationsdatei, die ein vom Collector initiiertes Abonnement erstellt, um Ereignisse aus dem Anwendungs Ereignisprotokoll eines Remote Computers an das ForwardedEvents-Protokoll weiterzuleiten.


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



Der folgende XML-Code ist ein Beispiel für eine Abonnement Konfigurationsdatei, die ein von der Quelle initiiertes Abonnement erstellt, mit dem Ereignisse aus dem Anwendungs Ereignisprotokoll eines Remote Computers an das ForwardedEvents-Protokoll weitergeleitet werden.


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
> Beim Erstellen eines von der Quelle initiierten Abonnements werden, wenn " **zugswedsourcedomaincomputers**", "zugswedsourcenondomaincomputers  / **issuercalist**", " **zugswedsubjetlist**" und " **deniedsubjetlist** " leer sind, standardmäßig ein Standardwert für "' o:NSG: nsd: (a;;  GA;;;D C) (A;; GA;;; NS) ". Diese SDDL-Standardeinstellung gewährt Mitgliedern der Domänen Gruppe "Domänen Computer" sowie der Gruppe "lokaler Netzwerkdienst" (für die lokale Weiterleitung) die Möglichkeit, Ereignisse für dieses Abonnement zu erhöhen.

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/Cun: *Benutzername***
</dt> <dd>

Ein-Wert, der die Anmelde Informationen für den freigegebenen Benutzer festlegt, die für Ereignis Quellen verwendet werden, die keine eigenen Anmelde Informationen besitzen. Dieser Wert gilt nur für vom Collector initiierte Abonnements.

> [!Note]  
> Wenn dieser Parameter angegeben ist, werden die Einstellungen für Benutzername und Kennwort für einzelne Ereignis Quellen aus der Konfigurationsdatei ignoriert. Wenn Sie andere Anmelde Informationen für eine bestimmte Ereignis Quelle verwenden möchten, können Sie diesen Wert überschreiben, indem Sie den/UN-Parameter und den/up-Parameter für eine bestimmte Ereignis Quelle in der Befehlszeile eines anderen Set-Abonnement-Befehls angeben.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *Kennwort***
</dt> <dd>

Ein-Wert, der das Benutzer Kennwort für die freigegebenen Benutzer Anmelde Informationen festlegt. Wenn *Password* auf " \* " (Sternchen) festgelegt ist, wird das Kennwort aus der Konsole gelesen. Diese Option ist nur gültig, wenn der/Cun-Parameter angegeben wird.

</dd> </dl>

## <a name="delete-a-subscription"></a>Löschen eines Abonnements

Die folgende Syntax wird verwendet, um ein Ereignis Abonnement zu löschen.

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>Lösch Parameter

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben. Das in diesem Parameter identifizierte Abonnement wird gelöscht.

</dd> </dl>

## <a name="retry-a-subscription"></a>Wiederholen eines Abonnements

Die folgende Syntax wird verwendet, um ein inaktives Abonnement zu wiederholen, indem versucht wird, alle oder angegebene Ereignis Quellen zu reaktivieren, indem eine Verbindung mit jeder Ereignis Quelle hergestellt und eine Remote Abonnement Anforderung an die Ereignis Quelle gesendet wird. Deaktivierte Ereignis Quellen werden nicht wiederholt.

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>Wiederholungs Parameter

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**
</dt> <dd>

Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert. Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben. Das in diesem Parameter identifizierte Abonnement wird wiederholt.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**Ereignis \_ Quelle**
</dt> <dd>

Ein-Wert, der einen Computer identifiziert, bei dem es sich um eine Ereignis Quelle für ein Ereignis Abonnement handelt. Bei diesem Wert kann es sich um den voll qualifizierten Domänen Namen für den Computer, den NetBIOS-Namen oder die IP-Adresse handeln.

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>Konfigurieren des Windows-Ereignis Sammler Dienstanbieter

Die folgende Syntax wird verwendet, um den Windows-Ereignis Sammlungs Dienst zu konfigurieren, um sicherzustellen, dass Ereignis Abonnements durch Neustarts von Computern erstellt und aufrechterhalten werden können. Dies umfasst das folgende Verfahren:

**So konfigurieren Sie den Windows-Ereignis Sammlungs Dienst**

1.  Aktivieren Sie den Kanal ForwardedEvents, wenn er deaktiviert ist.
2.  Verzögern Sie den Start des Windows-Ereignis Sammlungs Dienstanbieter.
3.  Starten Sie den Windows-Ereignis Sammler Dienst, wenn er nicht ausgeführt wird.

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>Ereignis Sammler Parameter konfigurieren

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *Wert***
</dt> <dd>

Ein-Wert, der bestimmt, ob der Quick-config-Befehl zur Bestätigung aufgefordert wird. Der Wert kann "true" oder "false" sein. Wenn value den Wert true hat, wird der Befehl zur Bestätigung aufgefordert. Der Standardwert ist „FALSE“.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

 





