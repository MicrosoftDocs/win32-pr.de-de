---
description: Die Kommunikation mit einem Netzwerkgerät mithilfe der WMI-SNMP-Schnittstelle erfordert die Konfiguration des Geräts, des SNMP-Diensts und des WMI-Diensts. In den Informationen in diesem Thema wird erläutert, wie Sie die WMI-SNMP-Umgebung einrichten.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Einrichten der WMI-SNMP-Umgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349228"
---
# <a name="setting-up-the-wmi-snmp-environment"></a>Einrichten der WMI-SNMP-Umgebung

Die Kommunikation mit einem Netzwerkgerät mithilfe der WMI-SNMP-Schnittstelle erfordert die Konfiguration des Geräts, des SNMP-Diensts und des WMI-Diensts. In den Informationen in diesem Thema wird erläutert, wie Sie die WMI-SNMP-Umgebung einrichten.

In diesem Thema werden die folgenden Abschnitte erläutert:

## <a name="installing-the-snmp-provider"></a>Installieren des SNMP-Anbieters

Der SNMP-Dienst ist standardmäßig nicht aktiviert. Sie können den SNMP-Dienst und den WMI-SNMP-Anbieter über die Systemsteuerung aktivieren. Beachten Sie, dass der SNMP-Dienst aktiviert und ausgeführt werden muss, damit der WMI-SNMP-Anbieter funktioniert.

Verwenden Sie ab Windows Vista das folgende Verfahren, um den SNMP-Anbieter zu installieren.

**So installieren Sie den SNMP-Anbieter**

1.  Wählen Sie in der **Systemsteuerung** **Programme** aus.
2.  Wählen Sie unter **Programme und Funktionen** die Option Windows-Funktionen ein- **oder ausschalten** aus.
3.  Scrollen Sie in der Liste Windows-Features nach unten zu **SNMP-Feature** , und erweitern Sie die Liste, sodass Sie den **WMI-SNMP-Anbieter** sehen können.
4.  Aktivieren Sie das Kontrollkästchen für den **WMI-SNMP-Anbieter**. Das Kontrollkästchen für das **SNMP-Feature** wird automatisch ausgewählt, da der Anbieter SNMP erfordert.
5.  Klicken Sie auf **OK**.
6.  Führen Sie an einer Eingabeaufforderung oder im **Startmenü** Services. msc aus, und vergewissern Sie sich, dass der SNMP-Dienst gestartet wurde.

## <a name="creating-an-snmp-namespace"></a>Erstellen eines SNMP-Namespace

Ein SNMP-Namespace definiert eine Ansicht eines Netzwerkgeräts.

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).

 

Im folgenden Verfahren wird beschrieben, wie Sie einen SNMP-WMI- [*Namespace*](gloss-n.md)erstellen.

**So erstellen Sie einen SNMP-Namespace**

1.  Erstellen Sie eine Instanz der [**\_ \_ Namespace**](--namespace.md) -System Klasse, indem Sie entweder eine [*Managed Object Format*](gloss-m.md) . MOF-Datei kompilieren oder die [com-API für WMI](com-api-for-wmi.md)verwenden.

    Weitere Informationen finden Sie unter [Erstellen von Hierarchien in WMI](creating-hierarchies-within-wmi.md).

2.  Ordnen Sie SNMP-Anbieter [*Qualifizierer*](gloss-q.md) der Namespace Definition zu.

    Die SNMP-Anbieter Qualifizierer enthalten Implementierungs spezifische Kontextinformationen und Transporteigenschaften, die definieren, wie der SNMP-Anbieter auf ein SNMP-Gerät zugreift. Weitere Informationen finden Sie unter [**Qualifizierer für den SNMP-Anbieter**](qualifiers-specific-to-the-snmp-provider.md).

3.  Verwenden Sie das Befehlszeilen Tool " [wfcomp](mofcomp.md) ", um den MOF-Code in das WMI-Repository zu laden.

    Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).

Im folgenden MOF-Codebeispiel \\ wird der SNMP--Namespace mit einer Teilmenge der Qualifizierer definiert, die einem SNMP--Namespace zugeordnet werden können.

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

Als Anbieter fungiert der SNMP-Anbieter als Brücke zwischen SNMP-Daten und WMI-Klassen. Daher müssen Sie über Klassen in WMI verfügen, die unterschiedliche Aspekte eines SNMP-fähigen Geräts darstellen. Hierzu müssen Sie den SNMP-Informationsmodul Compiler ([Smi2smir](smi2smir.md)) verwenden, um SNMP-Verwaltungsinformationen aus dem SNMP-Format in die entsprechenden CIM-Schema Definitionen zu kompilieren. Anschließend können Sie die Ausgabe des Informations Compilers in eine SNMP-Schema Datenbank mit dem Namen "SNMP Module Information Repository (SMIR)" oder mehrere verschiedene Arten von MOF-Dateien weiterleiten.

Der Compiler wird im Befehlszeilen Modus ausgeführt, wobei eine MIB-Datei als Eingabe verwendet wird. Mit dem folgenden Befehl wird die angegebene MIB-Datei in SMIR geladen.

**Smi2smir/a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>Einrichten von SNMP-Communitys

Als Sicherheitsmaßnahme wird die öffentliche SNMP-Community standardmäßig nicht erstellt. Sie können die Community erstellen, wie unter [](/previous-versions/windows/embedded/ms907028(v=msdn.10))communityregistrierungseinstellungen beschrieben. Wenn Sie keine Community haben, erstellen Sie die Public-Community für den Zugriff auf den SNMP-Anbieter.

## <a name="generating-mof-files-from-mib-files"></a>Erstellen von MOF-Dateien aus MIB-Dateien

Die folgenden Befehle sind ein Beispiel für das Generieren von MOF-Dateien aus den MIB-Dateien, die bei der Installation des SNMP-Anbieters installiert werden.

**CD** *% windir% \\ system32 \\ WBEM \\ SNMP*

**Smi2smir/g** *. \\ \\ .. hostmib. MIB* **>** *hostmib. MOF*

**Smi2smir/g** *. \\ \\ .. ipforwd. MIB* **>** *ipforwd. MOF*

**Smi2smir/g** *. \\ \\ .. nipx. MIB* **>** *nipx. MOF*

**Smi2smir/g** *. \\ \\ .. MIB \_ II. MIB* **>** *MIB \_ II. MOF*

**Smi2smir/g** *. \\ \\ .. lmmib2. MIB* **>** *lmmib2. MOF*

**Smi2smir/g** *. \\ \\ .. mcastmib. MIB* **>** *mcastmib. MOF*

**Smi2smir/g** *. \\ \\ .. rfc2571. MIB* **>** *rfc2571. MOF*

**Smi2smir/g** *. \\ \\ .. wfospf. MIB* **>** *wfospf. MOF*

**Smi2smir/g** *. \\ \\ .. DHCP. MIB.. \\ . \\ msft. MIB* **>** *DHCP. MOF*

**Smi2smir/g** *. \\ \\ .. WINS. MIB.. \\ . \\ msft. MIB* **>** *WINS. MOF*

**Smi2smir/g** *. \\ \\ .. mipx. MIB.. \\ . \\ msft. MIB* **>** *mipx. MOF*

**Smi2smir/g** *. \\ \\ .. mripsap. MIB. \\ \\ .. msft. MIB* **>** *mripsap. MOF*

**Smi2smir/g** *. \\ \\ .. msipbtp. MIB \\ \\ .... msft. MIB* **>** *msipbtp. MOF*

**Smi2smir/g** *. \\ \\ .. msiprip2. MIB.. \\ . \\ msft. MIB* **>** *msiprip2. MOF*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>Hinzufügen von SNMP-MOF-Dateien zum WMI-Repository

Die folgenden Befehle sind ein Beispiel dafür, wie die MOF-Dateien, die aus den MIB-Dateien generiert werden, dem WMI-Repository hinzugefügt werden. Wenn Sie die MOF-Dateien der Liste der Dateien hinzufügen möchten, die automatisch in einer Wiederherstellung des [*WMI-Repository*](gloss-w.md) wieder hergestellt werden sollen, fügen Sie am Ende jedes Befehls das Flag **-AutoRecover** hinzu. Weitere Informationen zum WMI-Mofcomp.exe Befehlszeilen Tool finden Sie unter " [**MUF**](mofcomp.md)".

" **mamacomp** *hostmib. MOF* "

" *ipforwd. mof" von* " **mumacomp** "

" **mamacomp** *nipx. MOF* "

" **mamacomp** *MIB \_ II. MOF* "

 *lmmib2. MOF* -Datei

" *mcastmib. mof" von* " **mumacomp** "

 *rfc2571. MOF* -Datei

**mufcomp** *wfospf. MOF*

" *DHCP. mof" von* " **MUF** "

" **mumacomp** *mipx. MOF* "

" *mrippsap. mof" von* " **MUF** "

" *msipbtp. mof" von* " **MUF** "

 *msiprip2. MOF* -Datei

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf SNMP-Geräte](accessing-snmp-devices.md)
</dt> </dl>

 

 
