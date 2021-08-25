---
description: Für die Kommunikation mit einem Netzwerkgerät über die WMI-SNMP-Schnittstelle ist die Konfiguration der Geräte-, SNMP- und WMI-Dienste erforderlich. In diesem Thema wird erläutert, wie Sie die WMI-SNMP-Umgebung einrichten.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Einrichten der WMI-SNMP-Umgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a090dab219c589fc8d9084c445e9a69c8d75afefb64400fe3029bfed66ab931
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860411"
---
# <a name="setting-up-the-wmi-snmp-environment"></a>Einrichten der WMI-SNMP-Umgebung

Für die Kommunikation mit einem Netzwerkgerät über die WMI-SNMP-Schnittstelle ist die Konfiguration der Geräte-, SNMP- und WMI-Dienste erforderlich. In diesem Thema wird erläutert, wie Sie die WMI-SNMP-Umgebung einrichten.

In diesem Thema werden die folgenden Abschnitte erläutert:

## <a name="installing-the-snmp-provider"></a>Installieren des SNMP-Anbieters

Der SNMP-Dienst ist standardmäßig nicht aktiviert. Sie können den SNMP-Dienst und den WMI-SNMP-Anbieter über die Systemsteuerung. Beachten Sie, dass der SNMP-Dienst aktiviert und ausgeführt werden muss, damit der WMI-SNMP-Anbieter funktioniert.

Ab Windows Vista verwenden Sie das folgende Verfahren, um den SNMP-Anbieter zu installieren.

**So installieren Sie den SNMP-Anbieter**

1.  Wählen Sie **im Systemsteuerung** die Option **Programme aus.**
2.  Wählen **Sie unter Programme und Features** die Option Windows Features aktivieren oder deaktivieren **aus.**
3.  Scrollen Sie Windows Liste der Features nach unten zum **SNMP-Feature,** und erweitern Sie die Liste, damit **der WMI-SNMP-Anbieter angezeigt wird.**
4.  Aktivieren Sie das Kontrollkästchen für **den WMI-SNMP-Anbieter**. Das Kontrollkästchen für **das SNMP-Feature** wird automatisch aktiviert, da der Anbieter SNMP erfordert.
5.  Klicken Sie auf **OK**.
6.  Führen Sie über eine Eingabeaufforderung **oder das Startmenü** Services.msc aus, und stellen Sie sicher, dass der SNMP-Dienst gestartet wird.

## <a name="creating-an-snmp-namespace"></a>Erstellen eines SNMP-Namespace

Ein SNMP-Namespace definiert eine Ansicht eines Netzwerkgeräts.

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente unter einem bestimmten Betriebssystem finden Sie unter [Betriebssystemverfügbarkeit von WMI-Komponenten.](operating-system-availability-of-wmi-components.md)

 

Im folgenden Verfahren wird beschrieben, wie ein SNMP-WMI-Namespace [*erstellt wird.*](gloss-n.md)

**So erstellen Sie einen SNMP-Namespace**

1.  Erstellen Sie eine Instanz der [**\_ \_ Namespace-Systemklasse,**](--namespace.md) indem Sie entweder eine Managed Object Format [](gloss-m.md) MOF-Datei kompilieren oder die [COM-API für WMI verwenden.](com-api-for-wmi.md)

    Weitere Informationen finden Sie unter [Erstellen von Hierarchien in WMI.](creating-hierarchies-within-wmi.md)

2.  Ordnen Sie der [](gloss-q.md) Namespacedefinition SNMP-Anbieterqualifizierer zu.

    Die SNMP-Anbieterqualifizierer enthalten implementierungsspezifische Kontextinformationen und Transporteigenschaften, die definieren, wie der SNMP-Anbieter auf ein SNMP-Gerät zutritt. Weitere Informationen finden Sie unter Für den [**SNMP-Anbieter spezifische Qualifizierer.**](qualifiers-specific-to-the-snmp-provider.md)

3.  Verwenden Sie [das Befehlszeilentool mofcomp,](mofcomp.md) um den MOF-Code in das WMI-Repository zu laden.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien.](compiling-mof-files.md)

Im folgenden MOF-Codebeispiel wird der snmp-Namespace mit einer Teilmenge der Qualifizierer definiert, die \\ einem SNMP-Namespace zugeordnet werden können.

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a>Einfügen von SNMP-MIB-Daten in WMI

Als Anbieter fungiert der SNMP-Anbieter als Brücke zwischen SNMP-Daten und WMI-Klassen. Daher müssen Sie über Klassen in WMI verfügen, die verschiedene Aspekte eines SNMP-fähigen Geräts darstellen. Hierzu müssen Sie den SNMP-Informationsmodulcompiler ([smi2smir](smi2smir.md)) verwenden, um SNMP-Verwaltungsinformationen aus dem SNMP-Format in die entsprechenden CIM-Schemadefinitionen zu kompilieren. Anschließend können Sie die Ausgabe des Informationscompilers an eine SNMP-Schemadatenbank mit dem Namen "SNMP Module Information Repository (SMIR)" oder an verschiedene Arten von MOF-Dateien weiter richten.

Der Compiler wird im Befehlszeilenmodus mit einer MIB-Datei als Eingabe ausgeführt. Der folgende Befehl lädt die angegebene MIB-Datei in SMIR.

**smi2smir /a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>Einrichten von SNMP-Communitys

Als Sicherheitsmaßnahme wird die "öffentliche" SNMP-Community nicht standardmäßig erstellt. Sie können die Community wie unter [Communitys Registry Einstellungen.](/previous-versions/windows/embedded/ms907028(v=msdn.10)) Wenn Sie keine Community haben, erstellen Sie die "öffentliche" Community für den Zugriff auf den SNMP-Anbieter.

## <a name="generating-mof-files-from-mib-files"></a>Generieren von MOF-Dateien aus MIB-Dateien

Die folgenden Befehle sind ein Beispiel für das Generieren von MOF-Dateien aus den MIB-Dateien, die bei der Installation des SNMP-Anbieters installiert werden.

**cd** *%windir% \\ system32 \\ wbem \\ SNMP*

**Smi2smir /g** *.. \\ . \\ hostmib.mib* **>** *hostmib.mof*

**Smi2smir /g** *.. \\ . \\ ipforwd.mib* **>** *ipforwd.mof*

**Smi2smir /g** *.. \\ . \\ nipx.mib* **>** *nipx.mof*

**Smi2smir /g** *.. \\ . \\ mib \_ ii.mib* **>** *mib \_ ii.mof*

**Smi2smir /g** *.. \\ . \\ lmmib2.mib* **>** *lmmib2.mof*

**Smi2smir /g** *.. \\ . \\ mcastmib.mib* **>** *mcastmib.mof*

**Smi2smir /g** *.. \\ . \\ rfc2571.mib* **>** *rfc2571.mof*

**Smi2smir /g** *.. \\ . \\ wfospf.mib* **>** *wfospf.mof*

**Smi2smir /g** *.. \\ . \\ dhcp.mib.. \\ .. \\ msft.mib* **>** *dhcp.mof*

**Smi2smir /g** *.. \\ . \\ wins.mib.. \\ .. \\ msft.mib* **>** *wins.mof*

**Smi2smir /g** *.. \\ . \\ mipx.mib.. \\ .. \\ msft.mib* **>** *mipx.mof*

**Smi2smir /g** *.. \\ . \\ mripsap.mib.. \\ .. \\ msft.mib* **>** *mripsap.mof*

**Smi2smir /g** *.. \\ . \\ msipbtp.mib.. \\ .. \\ msft.mib* **>** *msipbtp.mof*

**Smi2smir /g** *.. \\ . \\ msiprip2.mib.. \\ .. \\ msft.mib* **>** *msiprip2.mof*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>Hinzufügen von SNMP-MOF-Dateien zum WMI-Repository

Die folgenden Befehle sind ein Beispiel für das Hinzufügen der MOF-Dateien, die aus den MIB-Dateien generiert werden, zum WMI-Repository. Wenn Sie die MOF-Dateien der Liste der Dateien hinzufügen möchten, die bei einer [*WMI-Repositorywiederherstellung*](gloss-w.md) automatisch wiederhergestellt werden sollen, fügen Sie das Flag **-AUTORECOVER** am Ende jedes Befehls hinzu. Weitere Informationen zum WMI-Mofcomp.exe-Befehlszeilentool finden Sie unter [**mofcomp**](mofcomp.md).

**mofcomp** *hostmib.mof*

**mofcomp** *ipforwd.mof*

**mofcomp** *nipx.mof*

**mofcomp** *mib \_ ii.mof*

**mofcomp** *lmmib2.mof*

**mofcomp** *mcastmib.mof*

**mofcomp** *rfc2571.mof*

**mofcomp** *wfospf.mof*

**mofcomp** *dhcp.mof*

**mofcomp** *mipx.mof*

**mofcomp** *mripsap.mof*

**mofcomp** *msipbtp.mof*

**mofcomp** *msiprip2.mof*

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf SNMP-Geräte](accessing-snmp-devices.md)
</dt> </dl>

 

 
