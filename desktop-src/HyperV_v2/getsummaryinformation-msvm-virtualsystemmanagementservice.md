---
description: Gibt Zusammenfassungs Informationen für virtuelle Computer zurück.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Getsummaryinformation-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342799"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Getsummaryinformation-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Gibt Zusammenfassungs Informationen für virtuelle Computer zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SettingData* \[ in\]
</dt> <dd>

Typ: **CIM \_ virtualsystemsettingdata \[ \]**

Ein Array von [**CIM- \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Instanzen, die die virtuellen Computer oder Momentaufnahmen angeben, für die Informationen abgerufen werden sollen. Wenn dieser Parameter **null** ist, werden Informationen für alle virtuellen Computer abgerufen.

</dd> <dt>

*Requestedinformation* \[ in\]
</dt> <dd>

Typ: **UInt32 \[ \]**

Ein Array von Enumerationswerten, die den Eigenschaften in der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse entsprechen, die die Daten angeben, die für die im *SettingData* -Array angegebenen virtuellen Maschinen und Momentaufnahmen abgerufen werden sollen.

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name** (0)


</dt> <dd>

Dies entspricht der **Name** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Element Name** (1)


</dt> <dd>

Dies entspricht der **ElementName** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Erstellungszeit** (2)


</dt> <dd>

Dies entspricht der Eigenschaft " **kreationtime** " der Klasse " [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) ".

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Hinweise** (3)


</dt> <dd>

Dies entspricht der **Notes** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Anzahl der Prozessoren** (4)


</dt> <dd>

Dies entspricht der Eigenschaft " **numofprocessor** " der [**MSVM-Klasse " \_ SummaryInformation**](msvm-summaryinformation.md) ".

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Kleines Miniaturbild (80X 60)** (5)


</dt> <dd>

Dies entspricht der **thumbnailimage** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse. Ein Miniaturbild mit den Abmessungen 80 60 wird abgerufen.

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Bild für mittlere Miniaturansicht (160 x 120)** (6)


</dt> <dd>

Dies entspricht der **thumbnailimage** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse. Ein Miniaturbild mit den Abmessungen 160 120 wird abgerufen.

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Großes Miniaturbild (320 x 240)** (7)


</dt> <dd>

Dies entspricht der **thumbnailimage** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse. Ein Miniaturbild mit den Abmessungen 320 240 wird abgerufen.

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**Zugedgpu** (8)


</dt> <dd>

Dies entspricht der Eigenschaft " **zugseredgpu** " der [**MSVM-Klasse " \_ SummaryInformation**](msvm-summaryinformation.md) ".

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**Virtualswitchnames** (9)


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)


</dt> <dd>

> [!Note]  
> In Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Abgeschirmt** (11)


</dt> <dd>

> [!Note]  
> In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**Enabledstate** (100)


</dt> <dd>

Dies entspricht der **enabledstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**Processorload** (101)


</dt> <dd>

Dies entspricht der **processorload** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**Processorloadhistory** (102)


</dt> <dd>

Dies entspricht der **processorloadhistory** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**Memoryusage** (103)


</dt> <dd>

Dies entspricht der **memoryusage** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>Takt **(104** )


</dt> <dd>

Dies entspricht der **Heartbeat** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Betriebszeit** (105)


</dt> <dd>

Dies entspricht der Eigenschaft " **Uptime** " der Klasse " [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) ".

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**Guestoperatingsystem** (106)


</dt> <dd>

Dies entspricht der **guestoperatingsystem** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Momentaufnahmen** (107)


</dt> <dd>

Dies entspricht der **Momentaufnahmen** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**Asynchronoustasks** (108)


</dt> <dd>

Dies entspricht der **asynchronoustasks** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**Healthstate** (109)


</dt> <dd>

Dies entspricht der **healthstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)


</dt> <dd>

Dies entspricht der **OperationalStatus** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**Status Beschreibungen** (111)


</dt> <dd>

Dies entspricht der Eigenschaft " **Status Beschreibungen** " der [**MSVM-Klasse " \_ SummaryInformation**](msvm-summaryinformation.md) ".

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>Speicher **verfügbar** (112)


</dt> <dd>

Dies entspricht der **memoryavailable** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**Availablememorybuffer** (113)


</dt> <dd>

Dies entspricht der **availablememorybuffer** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Replikations Modus** (114)


</dt> <dd>

Dies entspricht der **replicationmode** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Replikations Status** (115)


</dt> <dd>

Dies entspricht der **replicationstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replikation healthtest Replica System** (116)


</dt> <dd>

Dies entspricht der **ReplicationHealth** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Anwendungs** Integrität (117)


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**Replicationstateex** (118)


</dt> <dd>

Dies entspricht der **replicationstate** -Eigenschaft der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse. Dies ist ein Array für alle Replikations Zustands Werte über die primäre und erweiterte Beziehung hinweg. 0 der Indexwert ist für die primäre Beziehung immer, und wenn die erweiterte Replikation aktiviert ist, wird Sie in Index 1 zurückgegeben.

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**Replicationhealthex** (119)


</dt> <dd>

Dies entspricht der **ReplicationHealth** -Eigenschaft der [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse. Dies ist ein Array für alle Replikations Integritäts Werte über die primäre und erweiterte Beziehung hinweg. 0 der Indexwert ist für die primäre Beziehung immer, und wenn die erweiterte Replikation aktiviert ist, wird Sie in Index 1 zurückgegeben.

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>" **Swap-FilesInUse** " (120)


</dt> <dd>

Dies entspricht der Eigenschaft " **shiapfilesinuse** " der Klasse " [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) ".

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**Integrationservicesversionstate** (121)


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**Replicationproviderid** (122)


</dt> <dd>

Dies entspricht der **Name** -Eigenschaft der [**MSVM \_ replicationprovider**](msvm-replicationprovider.md) -Klasse.

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**Memoryspansphysicalnumanodes** (123)


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**Integrationservicesversionstate** (132)


</dt> <dd>

Dies entspricht der **integrationservicesversionstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**Otherenabledstate** (132)


</dt> <dd>

Dies entspricht der **otherenabledstate** -Eigenschaft der [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) -Klasse.

</dd> <dt>



 (133)


</dt> <dd></dd> </dl> </dd> <dt>

*SummaryInformation* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **MSVM \_ summaryinformationbase**](msvm-summaryinformationbase.md)\[\]**

Ein Array von [**MSVM- \_ summaryinformationbase**](msvm-summaryinformationbase.md) -Instanzen, die die angeforderten Informationen für die virtuellen Computer und/oder Momentaufnahmen enthalten, die im *SettingData* -Array angegeben sind. Dieses Array verfügt über die gleiche Anzahl von Elementen wie das *SettingData* -Array. Jeder dieser Einträge enthält die **Name** -Eigenschaft, auch wenn diese Eigenschaft nicht angefordert wurde. Wenn der virtuelle Computer oder die Momentaufnahme nicht gefunden werden kann oder nicht verfügbar ist, ist die **Name** -Eigenschaft des entsprechenden zusammenfassenden Informations Eintrags leer.

Eigenschaften, die nicht im *requestedinformation* -Parameter angegeben sind, haben einen **null** -Wert.

> [!Note]  
> Der Datentyp wurde in Windows 10, Version 1703, von [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md)aktualisiert.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Beispiele

Im folgenden c#-Beispiel werden Zusammenfassungs Informationen angezeigt. Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[**MSVM- \_ SummaryInformation**](msvm-summaryinformation.md)
</dt> </dl>

 

